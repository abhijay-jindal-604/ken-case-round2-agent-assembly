# Round 2 answers: final drafts (25 Sep 2026)

Decisions taken by the team on 25 Sep (visible in the AI log):
- **Q7:** rename the agent. The team delegated the choice of name; **Pehle** was picked. The product stays **Paid Tuesday**, which keeps Round 1 continuity.
- **Logistics:** the revision is accepted. Logistics has no role in the money and two bounded supporting uses.
- **Q5:** the counterparty claim-state rail, built by **Setu**.
- **Q8:** **CRED**.
- **Form limits:** none shown, so the answers are drafted to a readable length.

Design calls made while drafting (flag any you want changed):
- **Q2 is scored L3, not L4.** The paperwork loop is L4-shaped, but the rubric scores the most consequential unasked act, and both money acts sit inside limits other people set.
- **The advance is non-recourse on the counterparty's decision and full-recourse on the claimant's own acts.** The claimant owes us nothing if a valid claim is denied, but does owe us if they misrepresented it, filed it twice, or keep a payout that landed with them. This is what "we underwrite" (R1) means in practice.
- **Standing rule at signup.** The claimant sets a band once, for example "auto-accept any advance of 85% or more". Offers inside the band are accepted without a prompt. This keeps R1's promise that we ask only at signup and when a query needs a fact.

Web-checked on 25 Sep:
- **Happay (Q8):** its travel-and-expense business was sold to MakeMyTrip in Nov 2024, and CRED kept the payments part. Q8 was rewritten around this.
- **CRED lending (Q8):** CRED owns an NBFC, NewTap Finance, and CRED Cash is co-lent with L&T Finance (Aug 2024).
- **NHCX (Q5):** built by NHA and live since June 2024. It routes claims between hospitals and payers, with a payment-status check for hospitals.

Only one [CHECK] remains, and it sits in the Q4 table: whether Delhivery will carry medical papers.

---

## Q1. Outcome (one sentence)

For every bill a claimant forwards, Pehle is accountable for putting 70–95% of its policy-valid amount into their bank account within one working day of the claim packet passing our completeness check, and for closing the claim only when the employer's or insurer's payout has reconciled to the rupee against that advance and the balance has reached the claimant.

---

## Q2. Level of autonomy

**L3.** Pehle's most consequential act without asking anyone is moving money in two directions:
1. **Paying out the advance** (up to the lending partner's per-claim and portfolio limits, and inside the band the claimant set at signup).
2. **Debiting the claimant's salary account** under the recovery mandate they signed, once Account Aggregator shows the employer's or insurer's payout has landed with them. The debit comes after the mandatory 24-hour pre-debit notice and never exceeds what is owed on that claim.

Both acts sit inside limits somebody else set: the lender sets credit limits, and the claimant sets the offer band and the mandate ceiling. That makes it L3.

The paperwork side works like L4. Pehle plans the filing, chases for weeks, answers queries, checks its own work against the money (a desk saying "approved" does not count until the rupees reconcile), and is judged on the reconciled outcome. We still score the whole agent at L3, because the rubric scores the riskiest unasked act and we chose to keep the money under outside limits.

**Always goes to a human:**
- writing off any amount
- any appeal beyond the first internal one (an ombudsman complaint needs the claimant's own signature)
- a fraud or duplicate flag
- a claim-state read that contradicts an earlier read or the money
- a desk that refuses to speak to an AI, or any call where a callback was promised
- a recovery mandate that is halted after three failed debits
- a reconciliation that does not match to the rupee

---

## Q3. States

The counterparty is the employer's finance desk (the corporate expense wedge) or the insurer/TPA (post-discharge health, the annexation). The states are the same for both.

```
 S0 Onboard ─► S1 Ingest ─► S2 Discover ─► S3 Policy match ─► S4 Complete? ──gap──► S4a fetch / ask claimant
                                                                  ▲   │                S4b originals pickup (only if paper demanded)
                                                                  └───┴─────────────────────┘
                                                                      │ complete
                                                                      ▼
 S5 Underwrite ─► S6 Offer (auto inside the claimant's band, else ask) ─► S7 Advance paid ─► S8 Filed (proof of SUBMISSION)
                                                                                                   │
                        ┌──────────────────────────────────────────────────────────────────────────┘
                        ▼
                 S9 Claim-state read  ◄────►  S10 Query loop
                        │ payout
          ┌─────────────┴──────────────┐
          ▼                            ▼
   S11a paid into the           S11b lands with the claimant (seen via AA, nobody asked)
   per-claim account                   ▼
          │                     S11c recovery: payment link → 24h notice → debit → retries
          └──────────────┬─────────────┘
                         ▼
               S12 Reconcile to the rupee, balance to the claimant, file sealed ─► S13 Board update
```

**Happy flow**

| # | State | Entry | What Pehle does | Exit | Owner · timer |
|---|---|---|---|---|---|
| S0 | Onboard | Claimant signs up | KYC; bank account verified by penny drop plus name match; one purpose-bound grant to "file and chase claims in my name"; Account Aggregator consent (monitor purpose, credit filter on the salary account, held by our lending partner); recovery mandate (UPI AutoPay tied to the salary account); the claimant's auto-accept band; a low-weight address check | All objects active | Claimant, once |
| S1 | Ingest | Consents active | Reads the forwarded expense inbox, WhatsApp-forwarded bills, and card/UPI debits via AA | Candidate expenses listed | Agent · continuous |
| S2 | Discover | New debit or bill | Matches each spend to claims already filed; flags what was never filed or is stuck | Unfiled claim found | Agent |
| S3 | Policy match | Unfiled claim | Reads the employer's published expense policy or the insurer's wording: eligibility, caps, filing deadline | Policy-valid amount and deadline set | Agent |
| S4 | **Pre-filing completeness** (R1's insight as a state) | Policy-valid claim | Runs this counterparty's checklist: stamps, signed bill, discharge summary, approval email. Any gap goes to S4a. If the counterparty demands paper originals, S4b books a doorstep pickup where the courier checks the packet against the checklist before taking it | Checklist passes | Agent · the clock for Q1 starts here |
| S5 | Underwrite | Complete packet | How fast this counterparty has paid us before (our board) + document confidence + claimant signals → advance %, fee, or decline | Offer terms or decline | Agent inside lender rules |
| S6 | Offer | Terms set | Inside the claimant's band: auto-accept and notify. Outside it: one yes/no. First claim against a new counterparty: an eSigned assignment goes out, with space for the counterparty's acknowledgement | Accepted | Agent / claimant |
| S7 | **Advance paid** | Accepted | Checks the float; one payout keyed on the claim id (it cannot pay twice); waits for SUCCESS + UTR | Money in the claimant's account | Agent · ≤1 working day from S4 |
| S8 | Filed | Advance paid | Files in our name under the grant, by portal, email or courier. Records **proof of submission** (portal receipt, email, or courier waybill + dated delivery proof) separately from **proof of completeness** (the counterparty's acknowledgement) | Submitted | Agent |
| S9 | **Claim-state read** | Filed | Chases the acknowledgement and then the payout. Email or portal first; a voice call only after a pre-call check (grant active, desk number on record, calling hours, not DND). Each read returns received / query / approved / scheduled / denied, amount, date, reference, person spoken to. **Every read stays "unconfirmed" until money reconciles** | Payout seen, or query raised | Agent · the counterparty's own median payout time from our board sets the cadence |
| S10 | Query loop | Counterparty asks for something | Answers from the claim file. Asks the claimant only for a fact it cannot have, in their language, by WhatsApp or voice after a PIN check | Query answered → S9 | Agent / claimant |
| S11a | Paid into the claim account | The counterparty acknowledged the assignment | Payout arrives in the per-claim collection account | → S12 | Rail |
| S11b | Lands with the claimant | No acknowledgement (**the expected default today**) | AA shows the credit on the salary account; nobody is asked | → S11c | Agent |
| S11c | Recovery | S11b | Payment link first; if unpaid in 48h, 24h pre-debit notice → debit of exactly the amount owed → up to 3 retries | Recovered | Agent |
| S12 | Reconcile | Money in | Matches payout UTR, advance UTR and recovery to the rupee; pays the claimant any balance above the advance; seals the claim file (grant, assignment, UTRs, call audio + transcript, courier proof, every human decision) | Ledger closed | Agent |
| S13 | Board update | Ledger closed | Adds a dated row: counterparty, filed-to-paid days, query count, amount approved vs claimed | Row live | Agent |

**Unhappy flow** (each has an entry, an action and an exit)

| # | Entry | Pehle's action | Exit |
|---|---|---|---|
| U1 | S4: the claimant can't produce a document | Files only the part the documents support; states the gap in the filing | Smaller advance, or decline |
| U2 | S3: over the cap or a policy mismatch | Advances only on the policy-valid part and tells the claimant which clause applies | S5 on the reduced amount |
| U3 | S4: filing deadline within 3 days and packet incomplete | Files anyway with the gap declared (a late claim is dead; an incomplete one can be fixed) | S8, no advance until complete |
| U4 | S4b: courier check fails, pickup fails or packet returned | Returns to S4 with the missing item named; after two failures, offers self-drop | S4 |
| U5 | S5/S7: lender limit reached | Queues the advance and still files and chases; tells the claimant the expected date | S8, then S7 when limit frees |
| U6 | S2/S5: duplicate, double-dipping or doctored-bill signal | **Human review. No advance** | Human decides |
| U7 | S9: vague answer ("we'll look into it") or no status | Records "no status", never infers one; schedules a re-chase in 3 working days; after 3 empty reads, writes to the desk head | S9 |
| U8 | S9: a desk refuses to speak to an AI, or the call ends with a promised callback | Transfers live to our ops number with the transcript; if nobody answers, creates a **human task due the same working day**; emails the eSigned authorisation | Human speaks to the desk → S9 |
| U8b | S9: an extracted field (reference no., date, amount) appears only in Pehle's own words, never in the desk's | Drops the field and asks again next read | S9 |
| U9 | S9: a read contradicts an earlier read or the money ("approved", then "we never got the bills") | **Human review; no state change on the claim** | Human resolves → S9/S10 |
| U10 | S9: call not placed (pre-call veto, IVR dead end, no answer) | Falls back to email/portal | S9 |
| U11 | S9: desk reads out a different claim number | Holds on our claim id, logs the mismatch, never takes that claim's status | S9 |
| U12 | S9: partial approval | Recovers what was paid; claimant owes nothing for the shortfall on a valid claim; flags the gap for appeal | S12 or U13 |
| U13 | S9: denial | Technicality denials (a test the treating doctor didn't order, a discount read as fraud, pre-approval timing) → first appeal with the treating doctor's note. Anything further → human, with the claimant's signature for grievance/ombudsman | Paid → S11, or write-off (human) |
| U14 | S8/S10: "we never received the bills" | Sends the dated delivery proof and submission receipt | S9 |
| U15 | Counterparty refuses to acknowledge the assignment | No per-claim account; runs on AA detection + recovery | S11b default |
| U16 | AA consent revoked or expired | Asks the claimant to confirm payout at each expected date; stops auto-debit | S11c by link only |
| U17 | Recovery mandate revoked, or halted after 3 failed debits | Human task; payment link; recourse only if the claimant kept money that was ours | Human |
| U18 | Claimant leaves the employer | Files every open claim at once; notifies the lender | S8/S9 |
| U19 | Reconciliation off by any amount | Ledger stays open; human review | S12 |

---

## Q4. Capability table

Status key:
- **EXISTS·V**: exists, and we verified it ourselves on 25 Sep.
- **EXISTS·D**: exists in the rail's documentation; not yet tested by us.
- **PARTIAL**: exists but does not fully do the job.
- **MUST BUILD**: missing from the rail.
- **OFF-RAIL**: we build it ourselves.

### Payments (Pine Labs, including Setu, a Pine Labs subsidiary): load-bearing

| Name | Used at | What you send it | What comes back | When it fails | What it must never do | What exists today | Status |
|---|---|---|---|---|---|---|---|
| `kyc_claimant` | S0 | PAN / Aadhaar OTP | verified identity | mismatch → stop | proceed unverified | Setu KYC, PAN, Aadhaar-lite (docs.setu.co/data/kyc) | EXISTS·D |
| `verify_claimant_account` | S0 | account + IFSC, or ₹1 reverse penny drop | holder name, name-match score | mismatch → ask claimant | pay an account not in the claimant's name | Setu "Bank Account Verification", "Name Match API" | EXISTS·D |
| `grant_agent_authority` | S0, S8 | claimant, agent id, purpose "file and chase claim", caps, expiry | signed grant token, revocation events | revoked → stop acting | act on any claim not named | Grantex purpose-bound grants via P3P (/ai/p3p/sdks) | PARTIAL: built for spending only |
| `watch_salary_credits` | S0, S1, S11b | AA consent: PERIODIC, purpose 104, DEPOSIT, credit filter | transactions (≤1 fetch/hour) | revoked/expired → U16 | read beyond the consented account and filter | Setu "Account Aggregator" consent object | EXISTS·D (only through our lending partner as FIU) |
| `register_recovery_mandate` | S0 | AutoPay plan `AS`, ceiling, TPV = salary account | subscription ACTIVE | expired in 4h / revoked → U17 | debit anything but a named claim's amount owed | Subscriptions API (/ps/api/v1/public/subscriptions) | EXISTS·D |
| `sign_claim_assignment` | S6 | assignment deed, claimant + counterparty signers, eStamp | per-signer status, signed PDF | signer lapses → U15 | stand in for consent beyond the named counterparty | Setu "Aadhaar eSign" + "eStamp" (up to 6 signers) | EXISTS·D (legal effect off-rail) |
| `check_float_balance` | S7 | none | funding balance | below threshold → U5 | pay out before checking | "Get Payout Balance" | EXISTS·D |
| `disburse_advance` | S7 | claim id as `clientReferenceId`, verified account, amount | SUCCESS/FAILED, UTR, webhook | FAILED → one retry on same key → human | pay one claim twice; exceed ₹10 lakh or the approved amount | "Create Payout API" `POST /payouts/v3/payments/banks` | EXISTS·D |
| `confirm_disbursal` | S7 | claim id / UTR | status, UTR | PENDING past SLA → human | say "paid" before SUCCESS + UTR | "List Payouts API" | EXISTS·D |
| `issue_claim_collection_account` | S6, S11a | order for the claim amount | virtual account, IFSC, expiry | payer ignores it | pose as the claimant's own account | "Bank Transfer / ECMS" Create Challan | PARTIAL: payer must choose to pay it; expires |
| `send_recovery_link` | S11c | amount owed, expiry | link, status | unpaid 48h → debit | ask for more than owed | "Payment Links"; Setu "WhatsApp Collect" | EXISTS·D |
| `collect_recovery_debit` | S11c | subscription id, amount owed | PDN notified → COMPLETED/FAILED | 3 fails → HALTED → U17 | debit before AA shows the payout landed; skip the 24h notice | "Subscription Notification", "Create Debit", "Create Merchant Retry" | EXISTS·D |
| `reconcile_to_rupee` | S12 | UTRs, claim ids | settlement lines, payout list | ≤3h lag; mismatch → U19 | close a ledger with an unexplained paisa | "Get Settlements by UTR", "List Payouts API", Setu "Reports API" | EXISTS·D |
| `assign_inbound_payment` | S6, S11 | claimant's signed instruction naming one reimbursement, payer, amount, destination | payer acknowledgement; payout routed to us | payer refuses → S11b | route any payment other than the named claim | **nothing.** Every mandate on the rail is a debit on the payer's own account; none lets a payee point someone else's payment at a third party | **MUST BUILD** |

### Voice (Gnani): real but secondary

| Name | Used at | What you send it | What comes back | When it fails | What it must never do | What exists today | Status |
|---|---|---|---|---|---|---|---|
| `gate_each_call` | S9 | our API receives `conversation_id`, number → we return greeting + claim context, or 400 | call placed or vetoed (10s timeout) | our API slow → no call → U10 | dial without an active grant, outside hours, or to a number not on the desk's record | "Dynamic Variables & Dynamic Messages" | EXISTS·D |
| `read_claim_state_by_call` | S9 | claim id, amount, filing date, claimant name | status read back and confirmed | vague → U7; wrong claim → U11; contradiction → U9 | treat a spoken "approved" as fact before money reconciles | Agent Builder prompt + guardrails | **EXISTS·V**: 8 chat tests on 25 Sep (clear, vague, wrong-claim, contradictory, data-fishing, Hinglish); 6 pass, 1 partial, 1 fail |
| `extract_claim_status` | S9 | disposition field (approved / pending / rejected / paid / unclear) + `payout_date`, `reference_no` | `disposition_result` and `post_call_extraction_v2` JSON | vague desk → `unclear` → U7. **Found in testing:** `reference_no` was filled from *our own* question when the desk never confirmed it | record a value the counterparty didn't say; a field is kept only if the desk's own turn contains it (we check the transcript) | "Writing a Disposition Prompt"; Analytics Config | **EXISTS·V**: 2 tests to webhook.site, clear → `approved, 2026-09-30`; vague → `unclear` |
| `handle_authority_challenge` | S9 | "who authorised you?" / "we don't talk to bots" | names the claimant, offers the written grant by email; on refusal, transfers to our ops number with the transcript | in our test, a default handoff promised a callback and ended the chat → U8 | promise a callback nobody owns | "Transfer to Agent": an LLM-judged transfer condition, per-route numbers and messages, "Send transcript on transfer" (seen configured, 25 Sep) | **PARTIAL**: the transfer exists; routing it to our human desk instead of the default promise is ours to configure and test |
| `receive_call_outcome` | S9 | webhook URL + method (+ header) | transcript with timestamps, disposition, `call_infra` call record, `rec_path` | duplicate delivery → key on `conversation_id` | act twice on one call | "Post-Call Trigger" (Update Agent) | **EXISTS·V**: fired on both tests |
| `fetch_call_record` | S9, S12 | `conversationId` | timestamped turns + MP3 | 404 → call marked non-evidential | cite a call without its audio | "Get Conversation Statistics", "Get Conversation Audio" | EXISTS·D |
| `disclose_recording` | S9 | greeting with disclosure + "on behalf of [claimant]" | disclosure in turn 1 of transcript | missing → call not used as evidence | continue recording after an objection | nothing built in | MUST BUILD (prompt + transcript check) |
| `navigate_counterparty_ivr` | S9 | IVR path, claim number to key in | reach a person | menu changed → U10 | key in anything but the claim's own identifiers | nothing: DTMF is collection-only | MUST BUILD |
| `place_chase_calls_at_scale` | S9 | many desks per day | calls | not self-serve | call a number not on record | "Trigger Test Call" (whitelisted, test only); campaign manager on request | PARTIAL |
| `verify_claimant_caller` | S10 | DTMF PIN/OTP | verified / not | wrong digits → WhatsApp | reveal status before verification | "DTMF Collection" | EXISTS·D |
| `collect_missing_fact` | S4a, S10 | the one fact the query needs | captured value | unreachable → WhatsApp | ask for anything the query doesn't need | Variables, Dynamic Variables | EXISTS·D |
| `speak_and_hear_indian_languages` | S9, S10 | text/audio; agents offer 12 Indian languages (incl. Odia, Assamese, Urdu), speech APIs 10 + Hinglish | audio / transcript | ≤3 languages per agent; Punjabi not offered for agents | clone a real person's voice | "Gnani Prisma v2.5" STT, "Gnani Timbre v2.5" TTS; agent language picker | **EXISTS·V**: APIs workspace used; agent language list seen. ₹27/hour STT, ₹27 per 10k TTS chars; a short test chat cost ~0.47 credits |
| `seal_call_evidence` | S12 | MP3 + transcript + call record | hash, timestamp, immutable copy | fetch fails → non-evidential | alter the original | nothing: no retention setting in the agent config, no hash; the Audit Logs page logged 0 entries after we created, saved and tested an agent | OFF-RAIL |

### Logistics (Delhivery): no role in the money; two bounded supporting uses (a stated revision of Round 1)

| Name | Used at | What you send it | What comes back | When it fails | What it must never do | What exists today | Status |
|---|---|---|---|---|---|---|---|
| `move_money` | none | none | none | none | none | nothing on this rail | **No role** |
| `check_pickup_serviceable` | S4b | claimant + desk pincodes | pickup Y/N, days | no service → self-drop | book into a non-serviceable pincode | "B2C Pincode Serviceability", "Expected TAT API" | EXISTS·D |
| `book_originals_pickup` | S4b | reverse pickup: claimant's door → desk address, order = claim id | waybill | fraud/capacity errors → human | ship anything the claimant didn't approve | "Shipment Creation" with `payment_mode: Pickup` | EXISTS·D (whether medical papers are allowed [CHECK]) |
| `doorstep_packet_check` | S4b | checklist: "stamped discharge summary present?", "original bills: count" | pickup only if all answers correct; photos | fail → U4 | treat the courier's check as clinical or legal validation | "RVP QC 3.0" | PARTIAL (built for product returns) |
| `fetch_submission_proof` | S8, U14 | waybill | dated delivery proof, signature | archived → poll earlier | call a delivery proof "complete filing" | "Download Document API" (EPOD); "Shipment Tracking" | EXISTS·D |
| `check_address` | S0, U6 | claimant address; bill issuer's address | valid/junk, premise-level, recent delivery | 50 calls/day on the free tier | lower an offer on a negative alone | Maps "Address Validation" `/validate`, "Address Verification" `/verify` | EXISTS·D |
| `prove_complete_filing` | S8 | packet manifest + delivery proof | counterparty's acknowledgement that the set is complete | silent → S9 | treat delivery as acceptance | nothing: delivery proof shows a package arrived, not what was in it | MUST BUILD (Q5) |

### Off-rail (ours)
- `detect_unfiled_expense` (S2): matches card/UPI debits to claims.
- `match_policy` (S3): reads the employer's or insurer's published policy.
- `underwrite_claim` (S5): our model plus lender rules.
- `payout_speed_board` (S5, S13): our own reconciled book.
- `seal_claim_file` (S12): Grantex's evidence-package format is a ready template.
- `lending_licence_and_capital` (S7): our lending partner.

---

## Q5. Fourth rail

**Yes: a counterparty claim-state rail. We want Setu to build it.**

**What it does.** With the claimant's consent, the employer's expense system or the insurer/TPA publishes each claim's state in machine-readable form:
- received
- complete, with the date the last document arrived
- query, with the missing item named
- approved, with the amount
- payout scheduled, with the date
- paid, with the UTR

It also carries one routing field: "an assignment to X has been acknowledged; pay this claim to account Y."

**Why it makes Pehle much more effective.** All three rails fail at the same point. Payments can see money but not claim state. Voice can only ask a person for it, and our tests showed why that is fragile: a desk that says "approved" and then "we never got the bills", or one that refuses to talk and triggers a callback promise we must then honour. And even a clean extraction can record a reference number that only our agent said and the desk never confirmed. Logistics can prove a packet arrived, not that the claim is complete. With the fourth rail:
- **S9** turns from a phone call into a read.
- **S8** gets a real "complete filing" date. This is our Round 1 insight made provable: the settlement clock starts at complete filing, and today only the counterparty knows when that was.
- **S11** gets routed payouts, so the recovery debit becomes a fallback rather than the default.
- **S5** underwrites on "approved" rather than on "filed".
- **The board** becomes checkable by the counterparties themselves.

**Why Setu.** A consented, many-publisher, one-spec rail is the Account Aggregator problem again, and Setu has solved it twice:
- It built AA gateway plumbing, where regulated institutions publish data under a consent artefact.
- It built biller-side BBPS infrastructure, connecting billers to one national bill-state spec.
- It already runs a bounded bill-payment agent on Claude and ChatGPT.

It is also inside Pine Labs, whose corporate-expense product sits in some employers' reimbursement flow. That puts claim state and payout routing next to the money, which is where the routing field has to act.

**Why NHCX isn't already this rail.** The National Health Claims Exchange (NHA, live since June 2024) routes claims between hospitals and insurers/TPAs, and lets a hospital check payment status. It does not reach a patient who paid and is claiming reimbursement, or their agent, and it covers no employer expenses. The new rail can reuse NHCX's claim format for health. It also needs expense platforms as publishers: Happay (now MakeMyTrip), Zoho Expense, Fyle and Pine Labs' own.

---

## Q6. Interface

Five people touch Pehle. Each gets one surface, not a chatbot.

**1. The claimant** (a salaried employee with a travel backlog, or a patient home with the bills).
- **Signup, once, about 6 minutes on the web:** KYC, bank check, one Aadhaar eSign (the grant to file in their name), an AA consent screen, and an AutoPay mandate approved in their own UPI app. Then one slider: "Auto-accept any advance of at least __%". After this, Pehle asks only when a query needs a fact from them.
- **Sending bills:** forward to a personal email address, or send a photo or PDF on WhatsApp. Most people send nothing, because S2 finds the unfiled spend from their card/UPI debits.
- **Offers:** "₹16,600 now; ₹1,300 more when Acme pays (our fee: ₹550)." Accepted automatically inside their band; one tap outside it.
- **One status link per claim,** no login, no pings. A timeline shows **what the counterparty said** (grey, with date and source) **separately from what the money confirms** (green, with the UTR). A spoken "approved" never turns green.
- **Questions, only when needed:** WhatsApp or a call in their language, after a PIN check, asking for exactly one missing fact.
- **Money events:** advance paid; payout seen; 24h notice before any debit, with a "pay by link instead" button; the balance paid out.

**2. The counterparty desk** (an employer's finance desk, or an insurer/TPA).
- **Email first:** the claim packet, the eSigned assignment with a space to acknowledge it, and the per-claim account to pay into.
- **Then a call** that opens with a recording disclosure and the claimant's name, and asks one thing: the claim's status.
- **The desk can ask for a person at any point.** The call transfers live to our ops desk with the transcript attached, or, if no one is free, the desk gets a callback the same working day. We added this after our test in which a desk's refusal triggered a default promise of a callback that nobody owned.

**3. Our ops reviewer.**
- A queue of human tasks, one per escalation type in Q2: contradiction, refusal, fraud flag, halted mandate, reconciliation mismatch, write-off, appeal.
- Each task opens the sealed claim file (grant, assignment, UTRs, call audio with transcript, courier proof).
- Each decision is written back into that file.

**4. The lending partner.** A portfolio view: exposure by counterparty, days outstanding, recovery rate. It is also where they set the per-claim and portfolio limits that make the money acts L3.

**5. Readers of the settlement-speed board.** Median filed-to-paid days per employer and insurer, built only from reconciled rows.

---

## Q7. Name

**Pehle.** Hindi for "first", because Pehle pays you first and chases the counterparty afterwards. It is one word a desk hears clearly on a Hindi or English call: "I'm calling from Pehle, on behalf of Asha Verma." It runs inside the product we named in Round 1, **Paid Tuesday**.

---

## Q8. Best chance of building an agent like ours

**CRED.** It holds the two things that are hard to get, and has just removed the conflict that stops everyone else:
- **The claimant:** its members are the salaried, creditworthy people whose travel and expense claims make our cleanest wedge.
- **Credit:** it has its own NBFC, NewTap Finance. Through CRED Cash, launched with L&T Finance in 2024, it co-lends to members in minutes. Our design needs a licensed lender behind the advance, and CRED already has one.
- **No conflict:** our Round 1 test was "who has lending and users without underwriting its own paying customer?" RazorpayX fails it, because the employer is its client. CRED bought Happay, an expense platform, in 2021, but sold Happay's travel-and-expense business to MakeMyTrip in November 2024. It no longer sells to employers, so it can advance against an employer's unpaid reimbursement without judging a client.

That sale is also what CRED lacks. When it let Happay's expense side go, it lost its view of claim state. It now has no way to know whether an employer has approved a claim, or an insurer has scheduled one. That gap is the fourth rail in Q5. The other gaps are the voice chase and a reconciled book of how fast each counterparty pays. Our design supplies all three.
