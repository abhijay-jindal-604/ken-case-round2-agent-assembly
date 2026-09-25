# Round 2 — "Agent Assembly": full context

Everything needed before we answer Round 2. Working mode: **staged** (1: this file ·
2: read each rail's docs · 3: answer). **Scope up, not down.** This is a
case/design round, not a build round.

Items tagged **[CHECK]** are leads to verify. Nothing tagged [CHECK] goes into a
submitted answer until it's confirmed.

---

## 1. The round

- **Round 2 = "Agent Assembly."** Closes **Fri 25 September 2026, 11:59 PM IST.**
- "Round 1 asked you for an idea sketch. Round 2 turns that sketch into a design:
  **an agent specified well enough that someone else could build it**, and **a clear
  statement of what the rails cannot do for you yet**. The strongest designs go to
  the next round, where the rails open up and you find out whether your design
  survives contact with them."
- Every team answers the same 8 questions, whatever its track. "The tracks split in
  the next round: Build teams go on to build their agent, and Strategy teams get a
  different problem statement." The next round is the **Build round**, "where the
  field thins out and the end comes into view."
- **Submit:** answers typed into the form, plus (optional) "a link to your
  conversation with whatever AI tool you used."
- **Stakes:** a ₹20 lakh pool, a ₹10 lakh grand prize, and a credit in The Ken's "map
  of India's agentic era" (published in October, read by founders, investors and
  operators).
- **Our opening:** *Getting your money back*: "Claims, reimbursements, refunds — the
  counterparty automated its collecting and left your claiming manual." About 6.63% of
  teams picked it.
- **Our track:** Product Strategy (locked). Strategy teams finish with "a fully
  specified build — complete flows, the segment map, the wall you hit and why."
  Both tracks are judged on "the quality of your evidence, the depth of your
  load-bearing rail, the specificity of your ask."

---

## 2. The eight questions (verbatim)

| # | Question | Format |
|---|---|---|
| 01 | What is the **outcome** your agent is **accountable** for? | **One sentence** |
| 02 | What is the **level of autonomy** your agent has? Score it L1 to L4. *"Your agent's level is set by the **most consequential thing it does without asking anybody**."* | L1–L4 |
| 03 | What are the **states** your agent goes through? Share the **happy flow and the unhappy flow**. Be as specific as possible, and illustrate with a diagram if you prefer. | Free, diagram allowed |
| 04 | On each of the three rails, what does your agent **leverage that already exists**, and what capabilities does it need that **don't exist and must be built**? Refer to the documentation for each rail. | Capability table |
| 05 | If you had a choice, does your agent need a **fourth rail** to become much more effective? What would that rail do? Which **Indian company** would you want to build it? | Free |
| 06 | How will a human interact with your agent? What's their **interface**? Be as specific as possible. | Free |
| 07 | What is the **name** of your agent? | Name |
| 08 | Which Indian company has the **best chance of creating an agent just like yours**? | Company |

Word limits: only Q1 has one ("one sentence"). Check the form itself for character caps.

### Autonomy levels (Q2)
- **L1**: Prepares things for the person. They still do the work.
- **L2**: Proposes a specific action every time. The person says yes or no to each one.
- **L3**: Acts on its own inside limits somebody set. The person deals with whatever falls outside those limits.
- **L4**: Plans several steps, does them, checks its own work, comes back when stuck, and is judged on whether the thing got done.

### Q4 example capability table (their exact columns)

| Name | Used at | Rail | What you send it | What comes back | When it fails | What it must never do | What exists today | Build status |
|---|---|---|---|---|---|---|---|---|
| `confirm_permission_status` | State 3 | Payments | customer reference, service identifier | whether it is active, the amount, how often, when it last ran | says so and stops, never assumes there is none | touch a permission the person has not named | [named as its documentation names it, and where you found it] | EXISTS |

What the table implies:
- Capabilities are named like functions and **tied to a state number from Q3**. So
  Q3's numbering has to be fixed first.
- "What exists today" uses **the rail docs' own name for the feature, plus where we
  found it**. When reading the docs, log exact names and URLs.
- "Must never do" is a guardrail per capability. This is where the design shows
  judgment.

### Rail documentation
- **Gnani (voice):** docs at https://docs.gnani.ai/ and platform at https://app.gnani.ai/. *"Sign up
  on the platform as well, since the documentation alone will not show you
  everything it does. You'll get free credits courtesy Gnani."*
- **Pine Labs (payments and authorisation):** https://www.pinelabs.com/docs
- **Delhivery (logistics):** Developer portal at https://one.delhivery.com/developer-portal/documents · Maps reference at https://www.delhivery.com/maps/reference
- Questions: support@the-ken.com

### Still to paste in (collapsed on the page when captured)
- The FAQ answers, especially "**Our agent needs something that does not exist. Do we lose marks?**" and "Do we have to build or test anything this round?"
- The full opening text for *Getting your money back* ("View Your Opening")
- The "Competition Updates" (+4)

---

## 3. How it's judged

The five criteria:
- **Evidence**: "Did a real person tell you this? Interviews, recordings, and what you found that you weren't looking for."
- **Creativity**: "fresh, counterintuitive, unique… This is usually where AI-generated solutions fail."
- **Clarity**: "communicated clearly? Is it specific?"
- **Feasibility**: "practical… implemented in a reasonable way?"
- **Thoroughness**: "meticulous and detailed?"

Plus:
- **(a)** Graded **relative to other teams in the same opening** on originality and insight.
- **(b)** Graded **against The Ken's internal frontier-AI solution** for our opening.
- **(c)** AI logs and chats are requested, "to rank and grade human versus machine
  contributions. We encourage the use of AI, but show your work."

**What this means for us:** the AI baseline for this opening will likely be "scan
email/SMS for money owed → auto-file → track → remind → escalate to the
ombudsman/consumer forum → notify." Anything that reads like that scores as
baseline. Our differentiators, to lean on in every answer:
1. We **pay first**: a 70–95% advance within a day. We don't just chase.
2. We **underwrite** off the document plus the counterparty's own published policy.
3. We trigger on the **unfiled** bill ("claimants lose before the clock starts").
4. The **payee-side mandate**: assigning an *inbound* payment.
5. The **settlement-speed board**, built from our own reconciled book.

Keep the human decisions visible in the AI logs. Never let AI invent quotes or data.

---

## 4. Our team

- **Abhijay Jindal**: both parents are doctors; his father is a spine
  surgeon/orthopaedician practising at GMCH-32 (a government hospital, Chandigarh).
- **Bhaskar Kumar Arya**: a close friend's MRI claim was denied over a pre-approval
  technicality.

---

## 5. What we submitted in Round 1 (public record; build on it, don't contradict it)

Working name: **"Paid Tuesday"**.

**Q1: Team.** Abhijay: watched patients get claims denied for reasons unrelated to
treatment. An insurer demanding an X-ray the orthopaedic evaluation never needed; a
discounted surgery treated as double-dipping or fraud. The losses are constant, small
and normalised. Bhaskar: a friend's clinically warranted MRI was denied because the
prior-authorisation wasn't cleared before the scan. The out-of-pocket cost ran into
thousands and became unrecoverable. *Team (50 words):* "Between us we've watched this
failure from both ends… We validated the pattern with 3 practising doctors (1
government setting, 2 private) before submitting: documentation-technicality and
pre-approval-timing denials came up unprompted in every conversation."

**Q2: Insight.** "Claimants lose before the clock starts. The people we spoke to
described resubmission loops — an unstamped bill, a missing summary — that occur
before a claim counts as filed. IRDAI reports 99.93% of health claims settled within
three months; that clock begins at complete filing. So our advance triggers on the
unfiled bill, not the filed claim."

**Q3: Six steps.**
1. Trigger: You forward one expense inbox or statement; we find money you never filed.
2. What it knows: Your employer's published T&E policy, and how fast that employer has paid us before.
3. What it does: Assembles the complete packet, advances 70–95% same day, then files and chases.
4. Who it deals with: The employer's finance desk, in our own name, under your one-time signed mandate.
5. What it asks you: Only at signup, then again only for facts a query needs from you.
6. How it knows it's done: The payout lands and reconciles to the rupee against what we advanced.

**Q4: Rails.**
- *Payments, load-bearing:* "Payments *is* the product: the advance out, the recovery in, and a claimant-signed disbursement mandate with an auditable trail, which is precisely the object Pine Labs' P3P and Grantex already model."
- *Logistics, no role:* "Every claim we touch is documents and money; the one physical leg in this opening, the return pickup, is a use-case we deliberately excluded."
- *Voice, real but secondary:* "Recovery is conducted by phone against finance desks and TPAs in Indian languages… lowers our cost per recovery rather than carrying the mechanism."

**Q5: Innovation rail: Payments.** "Missing: a payee-side mandate — the claimant
authorising, once, that a specific incoming reimbursement be routed to their
financing agent. Every Indian mandate today is a pull instrument on debits; nothing
lets a person assign an inbound payment."

**Q6: Customer asset.** "Read access to their expense inbox and card/UPI statement.
It's the only way we find money they haven't filed — and they're paid before they
file anything."

**Q7: Annexation.** "Post-discharge health reimbursement claims. ClaimBuddy owns them
at admission, inside partner hospitals; nobody serves the person already home with
the bills. We arrive with the payout-speed data and the cash."

**Q8: Never hand to an assistant.** "16 — Sticking to the goal. A flawless assistant
would hit the target on your behalf, and the whole value of that opening is that the
person did it themselves."

**Q9: Should have built it: RazorpayX.** It runs payroll and expense disbursement for
thousands of employers, so it sees the reimbursement run, holds the employee's
account, and already moves money on payday. It hasn't built this because its customer
is the employer: advancing against an employer's unpaid reimbursement means
underwriting your own paying client's slowness, plus lending risk a payments company
won't hold.

**Q10: Track: Product Strategy.**
- *The wall:* no licensed co-lending partner or first-loss capital pool yet. We
  originate and service; the balance sheet sits with a licensed partner. The
  concierge version: 20–25 real stuck claims hand-run, each underwritten manually
  against a published policy, each recovery reconciled. These are the first 25 rows
  of the settlement-speed board.
- *The hard bet:* can we judge "policy-valid, will be paid" well enough to advance the
  same day? Start with the archetype that underwrites cleanly: salaried T&E against a
  published corporate policy. **Metric: ≥97% gross recovery at ≤8% claimant haircut**
  (gross recovery and net margin after write-offs).
- *The segment map:* the wedge is corporate reimbursement backlogs; large insurance
  claims are the annexation. Every advance is a dated outflow and every recovery a
  dated reconciled inflow → a transaction-verified record of how fast each employer
  and insurer pays. It needs no counterparty's permission; insurer API access and
  auto-honour would move a counterparty up the board.

### Continuity rules
- Round 2 builds on these answers. If we revise one, it's a deliberate, stated revision.
- The Q2 insight must appear as a **state** in Round 2 Q3 (a pre-filing completeness step).
- Round 2 Q8 ("best chance of creating") is a different question from Round 1 Q9
  ("should have built"). The answer can be a different company, with different
  reasoning.
- Delhivery was "no role" in Round 1. Keep that unless the docs reveal a genuine
  logistics leg, and if they do, say so explicitly.

---

## 6. Evidence we have

**Primary:** 3 doctor conversations (1 government, GMCH-32; 2 private), early
September 2026. These are working notes written afterward, not recordings. Raised
unprompted:
- **Documentation-technicality denials**: the insurer demands a diagnostic (for example an X-ray) the treating doctor's evaluation didn't require.
- **"Discount = fraud"**: a discounted surgery is read as evidence of double-billing.
- **Pre-approval timing** (Bhaskar's friend's MRI): the claim was valid, but the paperwork happened at the wrong moment.

All three have the same shape: a substantively valid claim fails on a procedural step
*before* the insurer's settlement clock starts.

**Cited context (IRDAI via Business Standard / Business Today):**
- FY24: ~11% of health claims denied, ~6% pending (March 2024); ~₹26,000 cr disallowed/repudiated, up 19.10% on FY23.
- FY2024-25: ~99.93% of health claims settled within three months. Our answer: the clock starts at complete filing. Two more arguments we haven't used yet: "settled" includes fast rejections, and the average blends fast cashless claims with slow reimbursement claims.

**Gap:** the wedge is corporate T&E, and we have no primary evidence there yet.
New evidence gathered now is dated as new. Every interview needs consent;
quotes are published as age band + city, never a name.

---

## 7. Question-by-question working map (seeds, not answers)

### Q1: Outcome
- It must be one accountable, measurable outcome, not an activity. Material: "the
  payout lands and reconciles to the rupee against what we advanced."
- Framing choice: time-to-cash for the claimant ("owed money in your account within
  24h of forwarding the bill") and/or a closed, reconciled recovery loop. Include a
  unit and a clock.

### Q2: Autonomy
- Candidate consequential acts done unasked: disbursing the advance, filing and
  chasing in its own name, accepting a partial payout, appealing a denial, writing off.
- Likely **L4** overall (it plans, acts, verifies via reconciliation, and comes back
  when stuck; R1 step 5). Money-moving acts are **bounded L3** inside the lender's
  credit limits and the claimant's mandate.
- Scope up: a per-action autonomy ladder saying what's L4, what's L3-bounded, and what
  always escalates to a human.

### Q3: States (do this first; it numbers everything else)
Draft skeleton:
- S0 Onboard: KYC, mandate(s), inbox/statement consent
- S1 Ingest: inbox + card/UPI statement
- S2 Discover: unclaimed or stuck expenses
- S3 Policy match: the employer T&E policy or the insurer wording; eligibility and caps
- S4 **Pre-filing completeness** (the Q2 insight): missing stamp, bill or summary → fetch or ask
- S5 Underwrite: counterparty payout-speed prior + document confidence → advance % and haircut
- S6 Offer + consent: this claim's assignment confirmed
- S7 Advance disbursed
- S8 File with the counterparty (in its own name, under mandate), with a timestamped proof of filing
- S9 Chase: email, portal or voice
- S10 Query loop: answer the counterparty; ask the claimant only for facts the agent can't have
- S11 Payout lands (routed to us, or to the claimant → recovery)
- S12 Reconcile to the rupee; residual paid to the claimant; the ledger is closed
- S13 Board update

Unhappy branches (each needs an entry condition, the agent's action and an exit):
missing document the claimant can't produce · over-cap or policy mismatch · partial
approval · denial (appeal → grievance → ombudsman → write-off) · technicality denials
(X-ray / discount / pre-auth) · payout lands with the claimant, not routed · mandate
revoked · claimant leaves the employer · duplicate or double-dipping flag ·
counterparty silent past the SLA · filing deadline missed · doctored bill · lender
capital limit hit · reconciliation dispute · data consent expires.

Deliverable: a state diagram + a state table (state, entry, exit, owner, timer, data written).

### Q4: Capability table per rail (the load-bearing question)
The rail docs are read. Candidate rows, with each doc's own names and URLs, are in **§10.1 (Pine Labs, incl. Setu,
P3P, Grantex), §10.2 (Gnani) and §10.3 (Delhivery + Maps)**. §10.4 has the cross-rail summary. What remains is to
fill "Used at" once Q3 is locked, then merge and trim.
- **Payments is load-bearing.** The core must-build is **`assign_inbound_payment`**. R1's line holds against the docs
  in the sharper form "every mandate on the rail is a debit authorisation on the payer's own account; none lets a
  payee point someone else's payment at a third party" (§10.1).
- **Voice is real but secondary**: claim-state extraction and claimant queries; chase-at-scale and IVRs are gaps
  (§10.2 verdict).
- **Logistics: no role in the money; two bounded supporting uses** (originals pickup with dated EPOD as evidence of
  submission; Maps address checks as a low-weight feature). The table keeps an explicit **`move_money` → no role**
  row. This is a deliberate, stated revision of R1's "no role" (§10.3).
- Build-status vocabulary: **EXISTS / PARTIAL / MUST BUILD (on rail) / OFF-RAIL (we build)**.

### Q5: Fourth rail
Ranked from the §10.4 gaps:
- **Counterparty claim-state rail (lead).** Machine-readable received / complete / approved / scheduled / paid, plus
  the payout's routing, from insurers and employers. This is the one gap all three rails share: payments can't see
  it, voice can only ask for it, and a POD can't prove it. It would also make `prove_complete_filing` and native
  payout routing possible. Health: NHCX [CHECK]. T&E: expense platforms (Zoho Expense, Happay, Fyle; Pine Labs'
  corporate-expense product [CHECK]).
- **Credit/lending rail**: co-lending with an NBFC, OCEN, receivables factoring. The advance *is* credit, but this is
  closer to a licence than a rail.
- **Document-authenticity rail**: DigiLocker coverage of medical documents [CHECK], digitally signed discharge
  summaries.
- Dropped as a Q5 candidate: the **consented-data rail**. Setu's Account Aggregator already sits inside rail 1 (§10.1).

### Q6: Interface
- The humans involved: the claimant · the counterparty finance desk or TPA · our
  underwriting/ops reviewer · the lending partner · board readers.
- Claimant touchpoints: onboarding (KYC, consent, mandate) · forwarding bills by
  email or WhatsApp · the offer screen ("₹X now, ₹Y when they pay") · mandate approval
  in their UPI app · query prompts only when a fact is missing · payout and residual
  notifications · a voice option in Indian languages.
- R1 constraint: it asks only at signup and when a query needs a fact. So status
  needs to be checkable without pings. Not a generic chatbot.

### Q7: Name
- "Paid Tuesday" is the working name. Keep it or name the agent separately, but keep
  continuity with R1.

### Q8: Best chance of building it
Candidates to weigh [CHECK facts]:
- **CRED**: affluent salaried users, lending, and Happay (expense management).
- **Pine Labs**: owns the rails.
- **Razorpay**: the R1 pick, conflicted.
- **PhonePe / Paytm**: UPI scale, insurance, lending.
- **Policybazaar, Plum, Onsurity, ClaimBuddy**: claims and benefits.
- **Bajaj Finserv**: NBFC plus insurance.

The test: who has a lending licence and users, **without** the conflict of
underwriting their own paying customer.

---

## 8. Research backlog

**A. Rail docs (next session).** One notes section per rail, capturing: products and
APIs by exact name + URL · inputs, outputs, statuses, webhooks, limits, failure codes
· what a "permission" or mandate object looks like · sandbox access · anything
agentic · candidate Q4 rows · gaps (these feed MUST BUILD and Q5). Order: **Pine Labs
→ Gnani (docs + platform) → Delhivery (portal + Maps).**

**B. Regulation and law [CHECK]:**
- RBI Digital Lending Directions
- RBI co-lending framework
- Factoring Regulation Act 2011 (amended 2021) / TReDS
- Transfer of Property Act s.130 (assigning an actionable claim with notice to the debtor), a possible legal basis for the payee-side mandate
- IRDAI Master Circular on Health Insurance (2024): settlement timelines, penal interest, whether the insurer or TPA must collect documents itself
- IRDAI and RBI regulatory sandboxes
- Whether insurance claim proceeds can be assigned
- DPDP Act 2023 (consent)

**C. Market [CHECK]:**
- The size of the corporate T&E reimbursement float (bottom-up estimate)
- Adjacent players: ClaimBuddy, the Policybazaar claims desk, claim consultancies, expense SaaS, earned-wage-access apps (the closest financial analogue: they advance against salary, not a specific receivable)

**D. Evidence to gather:**
- Salaried employees on T&E backlogs (this closes our biggest gap)
- Finance and HR desk staff (would they honour an assignment notice?)
- A post-discharge reimbursement claimant
- An NBFC, factoring or EWA operator (cost of capital, appetite)

---

## 9. Order of work
1. Rail docs: read (§10.1–§10.3; cross-rail summary §10.4).
2. Paste in the FAQ answers, the opening text and the competition updates.
3. Lock the Q3 state machine, starting from §7's skeleton plus the §10.4 changes (S0 objects, S4 physical branch,
   S8 submission vs completeness, S9 as a claim-state read, S11a/b/c, new unhappy branches).
4. Build the Q4 table against the Q3 state numbers from the §10 candidate rows.
5. Q1 + Q2 → Q5 (from the §10.4 gaps) → Q6 → Q7 + Q8.
6. Check the form's limits, do a final pass for sameness with the AI baseline, and attach the AI-log link.

---

## 10. Rail documentation, read in full (Stage 2, 24 Sep 2026)

Read before any design. Names below are the docs' own names; paths are the docs' own
paths. Anything the docs don't state is tagged [CHECK] or listed as a gap.
Build-status vocabulary as in §7: **EXISTS / PARTIAL / MUST BUILD (on rail) / OFF-RAIL (we build)**.

### 10.1 Pine Labs (payments and authorisation)

**Where the docs are.** https://www.pinelabs.com/docs is a hub with four portals:
- **Online Payments** (the API docs that matter): https://www.pinelabs.com/docs/online-payments/ ·
  index at `/docs/online-payments/llms.txt` (v2.1.0, updated 2026-07-21) · every page is
  also served as Markdown by appending `.md` · Postman/OpenAPI at
  `/docs/online-payments/developer-tools/postman-collections`.
  Base URLs: production `https://api.pluralpay.in`, sandbox (UAT) `https://pluraluat.v2.pinepg.in`.
  ("Plural" is the old brand name of Pine Labs Online; it still appears in hosts and some text.)
- **Instore/POS**: https://developer.pinelabs.com/in/instore (POS billing integration; not relevant).
- **Prepaid Issuance**: https://developers.qwikcilver.com/ (gift cards, prepaid; not relevant).
- **Fintech Infrastructure**: its "View API documents" buttons go to **https://docs.setu.co/**.
  Setu is Pine Labs (see "Setu" below), so Setu's APIs are part of this rail.

**Setu is part of Pine Labs (confirmed).** Pine Labs' own press release (10 Dec 2025,
https://www.pinelabs.com/media-analyst/setu-launches-indias-first-agentic-bill-payments-experience-on-chatgpt-and-claude):
"Setu, a brand of BrokenTusk Technologies Private Limited which is a wholly owned
subsidiary of Pine Labs Limited." The release names Setu's lines as eKYC, online contract
execution, Account Aggregator, UPI, and bill/loan/insurance/recurring collections.

#### Full product and API list (Online Payments docs, exact names)
- **Accept payments:** Hosted Checkout · Custom Checkout (Seamless) · iFrame Checkout ·
  Payment Links · Mobile SDKs (Android, iOS, React Native, Flutter) · Web SDKs · Server
  SDKs (.NET, Go, Java, Node.js `pinelabs-node`, PHP, Python, Ruby) · e-commerce plugins
  (Shopify, WooCommerce, Magento, OpenCart).
- **Payment methods:** Cards (3DS, tokenisation, pre-authorisation) · UPI (Collect,
  Intent/QR) · Net Banking · Wallets · Brand Wallet · Pay by Points · **Bank Transfer / ECMS
  (e-challan)** · **Third Party Validation (TPV)** · **UPI One-Time Mandate** · **UPI Reserve Pay
  (SBMD)** · Apple Pay · international (DCC, MCC, PA-CB import payments).
- **Affordability Suite:** credit/debit card EMI, down-payment EMI, Cardless EMI, BNPL,
  Instant Cashback on UPI, offer discovery/validation, IMEI validation.
- **Money-movement products:** **Payouts** · **Subscriptions** (plans, subscriptions,
  presentations) · **Split Settlements** · **Settlements** (T+1, early batch, same-day,
  holiday/weekend) · **Refunds** · Convenience Fees · Tokenization · Customers.
- **API reference groups:** Authentication (Generate Token) · Orders (Create, Get by ID, Get
  by Merchant Reference, Capture, Cancel) · Refunds (Create Refund) · Settlements (Get All
  Settlements, Get Settlements by UTR) · Split Settlements (Release Settlement, Cancel
  Settlement) · Affordability Suite · Card Payments (Create Payment, OTP, Decoupled
  Authorization) · E Challans (Create Challan, Get Challan, Get Challan PDF) · Apple Pay ·
  International Payments (MCC, Compute TCS, Capture Invoice, Upload Invoice File, AWB) ·
  BNPL (Check BNPL Eligibility) · Payment Option (Verify VPA) · Convenience Fee · Checkout
  (Generate Checkout Link) · Payment Links (Create, Get by ID/Merchant Reference, Cancel,
  Resend Notification) · Customers · Tokenization · **Payouts** (Create Payout, Get Payouts,
  Get Account Balance, Create Bulk Payouts, Update/Cancel Scheduled Payout) · **Subscriptions
  Plans / Subscriptions / Presentations** (incl. Subscription Notification, Create Debit,
  Create Merchant Retry) · **UPI Reserve Pay** · Brand Wallet / Brand Wallet Payments.
- **Developer tools:** Webhooks (events, retry policy, signature verification) · Error Codes
  (common, per-method, full list) · Test Cards · IPs & Ciphers · **Pine Labs CLI**.
- **AI:** **MCP Server** · **Agent Enablement Toolkit** · **Agent Skills** · **Pine Labs
  Payments Protocol (P3P)** · Agentic Commerce Suite · n8n node.
- **Marketing-site products with no Online API docs:** Instant Payouts, Fee Collection,
  Payment Forms, UPIverse; Credit Processing (Card Management, Card Switch, Co-brand
  Credit Card, UPI Issuer Switch, Credit Line on UPI, Clearing and Settlement, Payment
  Facilitator, Bharat Connect Switch, UPI Setu Acquirer Switch); prepaid (gift, reloadable,
  transit, forex, refunds-as-prepaid, rewards); Fintech Infrastructure (BBPS, Identity as a
  Service, Account Aggregator Gateway, Underwriting and Collections, UPI Collection, UPI
  Autopay; API docs = Setu).

#### Setu API list (docs.setu.co; index `/llms.txt`; pages as Markdown via `.mdx`)
- **Data and identity:** **Account Aggregator** (consent object, multi-AA gateway, FI data
  types, consent flow, data flow, notifications) · **Setu Insights** · **Signal IQ** (one
  orchestrated AA/PDF → insights flow) · **Aadhaar eSign** (+ **eStamp**, flexible eSign, PDF
  templating, eSign Name Match) · **DigiLocker** · **Bank Account Verification** (penny drop
  sync/async, **reverse penny drop**, bundled BAV) · **Name Match API** · KYC (PAN, Aadhaar-lite,
  GST, eKYC) · ULI.
- **Payments:** **UPI Setu** (UMAP: collect, Flash QR, TPV, VPA verification, refunds and
  disputes, transaction monitoring) · **UPI mandates** (OneShot = one-time, Recur, Reserve,
  ReservePlus = single block multi-debit; pause/unpause/update/revoke) · **UPI Deeplinks** ·
  **BBPS** (biller side, "Collect BBPS") · **BBPS BillPay** (customer side; COU APIs) ·
  **MCP Server for Bill Payments** · **WhatsApp Collect** (reminders, collection journey).
- **Tools:** **The Bridge** (dashboard, sandbox keys, reports) · **Reports API**.

#### P3P and Grantex: what they actually are
- **P3P = "Pine Labs Payments Protocol"** (one page also says "Pine Labs Machine Payment
  Protocol"). Docs: `/ai/p3p`, `/ai/p3p/quickstart`, `/ai/p3p/sdks`. "An open payments
  protocol that enables AI agents, merchants, and autonomous systems to securely initiate,
  authorize, and execute payments without a human at the point of transaction."
  - Mechanism: HTTP **402 Payment Required**. The paid server returns a challenge in
    `WWW-Authenticate`; the client SDK creates a one-time scoped token, retries with
    `P3P-Credential: Payment`; the server captures and returns a `Payment-Receipt` header
    ("cryptographically verifiable receipt… proof of payment for audit trails, compliance,
    and dispute resolution").
  - The payer's side is a **mandate** the customer approves up front ("customer-approved
    payment capacity"). Live on **UPI ReservePay**, **One Time Mandate** and **Cards**
    (pre-auth + captures); stablecoin is "future scope"; net banking/wallets/EMI "on the roadmap".
  - SDKs: `p3p-client-sdk` / `p3p-server-sdk` (npm), `pinelabs-online-p3p-client-sdk` /
    `pinelabs-online-p3p-server-sdk` (PyPI). Methods: `createMandate`, `getMandateBalance`
    (`GET /mpp/v1/balance`, ReservePay only), `getDebitStatus` (`GET /mpp/v1/debit/{id}`,
    SUCCESS/FAILED), `decidePayment` (402 → verify → capture; 202 "pending"),
    `createGrantexAuthorization`, `exchangeGrantexCode`, `allocateGrantexBudget`,
    `debitGrantexBudget`.
  - Protocol objects: Mandate · Challenge · Token · Credential · Capture · Mandate Balance ·
    Receipt · Grant.
- **Grantex is not a Pine Labs product.** It is "an open-source delegated authorization
  protocol and reference implementation for AI agents… owned by Orchestrum Technologies
  LLP" (https://grantex.dev, docs https://docs.grantex.dev, Apache-2.0, protocol v1.0, IETF
  individual draft `draft-mishra-oauth-agent-grants`). P3P uses it as the human-consent
  layer: the merchant signs up at grantex.dev, creates an Agent with scopes
  `mpp:payment:initiate` and `mpp:payment:max_txn_paise:*`, sends the user to a Grantex
  consent URL, exchanges the code for a **grant token** (JWT), optionally allocates a budget
  in paise, and sends `X-Grantex-Token` on every paid request (`enforceGrant: true`).
  - Grant token claims: `sub` (the human principal), `client_id` (agent), `scope`, `exp`,
    `jti` (for revocation), `urn:grantex:grant.grant_id`, `agent_did`, optional `act`
    delegation chain, `authorization_details` (purpose, tools, caps, budget).
  - Other Grantex features relevant to us: **Purpose-Bound Grants** (a grant carries one
    purpose from a controlled vocabulary, including `payments.payout`, plus private
    `x-<org>.<term>` purposes; tools can refuse other purposes) · **Caps and Metering** ·
    **Evidence and Verification** (a per-case JSON evidence package: grant chain, tool calls,
    human decisions, revocations, in a hash chain the service anchors and signs; verifiable
    offline with `grantex evidence verify`) · revocation (cascade, irreversible) and suspend ·
    a **DPDP & GDPR Compliance Module** (structured consent records, purpose limitation,
    withdrawal, audit exports).
  - Grantex's own docs say payment execution, mandate setup and receipts are
    "provider-owned" (Pine Labs Plural/P3P); Grantex only carries evidence references.
- **Verdict on our R1 line** ("a claimant-signed disbursement mandate with an auditable
  trail, which is precisely the object Pine Labs' P3P and Grantex already model"):
  P3P + Grantex model **a human-consented, scoped, capped, revocable authority for an agent
  to spend the human's own money, with a verifiable receipt per payment and an audit
  trail.** They do **not** model money coming *to* the claimant, or routing a third party's
  payment. What carries over: the pattern (consent → scoped grant → per-action receipt →
  audit package) and Grantex's purpose-bound grant, which can express "this agent may file
  and chase claim X in my name" [CHECK: nothing in the docs shows it used outside payments].
  Round 2 should state this precisely.

#### Test of our R1 line: "every Indian mandate today is a pull instrument on debits; nothing lets a person assign an inbound payment"
Every mandate-like object in the Pine Labs and Setu docs, checked:

| Object (docs name) | Direction | What it can do for us |
|---|---|---|
| Subscriptions / UPI AutoPay (plan `frequency` incl. `AS` and `OT`); mandate types One Time, On Demand, Recurring | Pull from the payer's own account | Recovery fallback: on-demand debit of the claimant after the payout lands with them |
| UPI One-Time Mandate (OTM) | Pull (funds blocked in the payer's account, one capture) | Block up to ₹1 lakh for ≤60 days; the customer cannot revoke from the UPI app |
| UPI Reserve Pay (SBMD) / Setu ReservePlus | Pull (block once, many debits) | ₹10,000 cap (NPCI); too small |
| eNACH (Fintech Infra page; Setu "Automated NACH via AA") | Pull | Same as AutoPay, for larger amounts [CHECK limits; no Online API page] |
| P3P mandate + Grantex grant | Pull (agent spends the user's money) | Pattern only |
| Payouts | Push from our own funded account | The advance |
| Bank Transfer / ECMS e-challan (`virtual_account_id`) | Inbound **collection address**, merchant-owned | A per-claim account the payer *could* pay into; the payer has to choose to |
| Split Settlements (`split_info`, `on_hold`, Release Settlement) | Allocates inbound money, but only pay-ins through our own Pine Labs order | Could split a recovery that is paid to us between lender and claimant residual |
| Settlements by UTR field `total_loan_recovery_amount` | Deduction from a merchant's own settlement | A precedent for deduct-at-source, for merchants only. Undocumented [CHECK] |
| Setu Account Aggregator consent | Read-only | Can *see* a credit land in the claimant's account (below) |

**Result: the R1 line holds against these docs.** Every mandate object is an authorisation
the *payer* gives over their *own* account. No object lets a payee redirect, assign or
split a payment that a third party (employer, insurer) sends. Precise wording for Round 2:
"every mandate on the rail is a debit authorisation on the payer's own account; none lets a
payee point someone else's payment at a third party." The closest pieces (virtual account,
split-settlement hold/release, AA credit monitoring, on-demand debit) can be combined into
a workaround, but each needs either the payer's cooperation or a pull from the claimant
after the money lands.

#### Relevant capabilities in detail

**Payouts (the advance out).** API ref `/api/payouts/*`.
- `POST /payouts/v3/payments/banks`, "Create Payout API". Send: `clientReferenceId` (1–40
  chars, **the idempotency key**), `payeeName` (letters/spaces, ≤40), `email`, `phone`,
  `accountNumber` + `branchCode` (IFSC) for IMPS/NEFT/RTGS or `vpa` for UPI, `amount`
  {`value` in paise, **₹1–₹10 lakh**}, `mode` `UPI|IMPS|NEFT|RTGS`, `remarks` (≤50,
  A-Z a-z 0-9 hyphen space). Headers `Request-Timestamp`, `Request-ID`. Returns `201`; errors
  `400/401/403/409/500`.
- `GET /payouts/v3/payments` "List Payouts API", by `paymentReferenceId`,
  `clientReferenceId`, `requestReferenceId`, `bankTransactionReferenceId` (UTR), mode,
  status, dates. Returns amount, fees, tax, UTR, `status` **SCHEDULED / PENDING / PROCESSING
  / PROCESSED / SUCCESS / FAILED**, `message`, timestamps.
- `GET /payouts/v3/payments/funding-account` "Get Payout Balance" (only if a funding
  account is linked). Bulk: `POST /payouts/v3/payments/banks/file` (async). Scheduled
  payouts can be updated or cancelled only while SCHEDULED.
- Webhooks: `payout-transaction-success`, `payout-transaction-failed` (`eventSource`
  PAYOUT; example failure message "Beneficiary Account blocked/frozen").
- The dashboard has a low-balance alert and an "Enable Payout Module" setting ("may require
  commercial activation"). No maker-checker or approval step is documented for the API.

**Recovery pull: Subscriptions / UPI AutoPay** (`/subscriptions/*`, API `/ps/api/v1/public/...`).
- Plan: `frequency` `Day|Week|Month|Year|Bi-Monthly|Quarterly|Half-Yearly|AS|OT|Not Applicable`
  (`AS` = amount/timing as presented; `OT` = one-time), `amount`, **`max_limit_amount`**
  (₹1–₹10 lakh field range), `end_date`, `merchant_plan_reference` (idempotency).
- Subscription: `plan_id`, `customer_id`, `start_date`/`end_date`,
  `allowed_payment_methods`, **`is_tpv_enabled` + `bank_account`** (ties the mandate to one
  named account), `merchant_subscription_reference` (idempotency).
- Mandate statuses: CREATED · EXPIRED (no bank response in 4 h) · INACTIVE · TRIAL · ACTIVE ·
  PAUSED · RESUMED · UPDATING · DEBIT FAILED · HALTED · CANCELLED · COMPLETED.
- Debit: Subscription Notification (pre-debit notification, "at least 24 hours before any
  debit"; up to 10 delivery retries; PDN FAILED) → Create Debit → COMPLETED/FAILED; Create
  Merchant Retry (max 3; then HALTED).
- Webhooks: SUBSCRIPTION_ACTIVATED / PENDING / PAUSED / RESUMED / COMPLETED / CHARGED /
  HALTED / CANCELLED / REVOKE_FAILED / UPDATED / UPDATE_FAILED.
- Feature list says "**Non Revocable Mandate Setup** — Create non-revocable UPI Autopay
  mandates. No mandate modification by customers post mandate setup." No API field for it
  appears [CHECK how it is enabled and which merchant categories qualify].
- The glossary says e-mandates are "governed by RBI guidelines on maximum debit amounts"; no
  number is given in the Online docs [CHECK the current AutoPay limit].

**UPI One-Time Mandate** (`/one-time-mandate/*`): block up to **₹1 lakh** (general
categories) for up to **60 days**; one capture; partial capture allowed and the remainder
released; no pre-debit notification; "the customer cannot revoke an active OTM directly from
a TPAP app". Setu equivalent: UPI Setu **OneShot**.

**Bank Transfer / ECMS** (`/payments-e-challan`, API `/api/e-challans/*`).
`POST /api/pay/v1/order/{order_id}/challan` → `challan_id`, `virtual_account_id`,
`account_name`, `account_ifsc`, `account_bank_name`, `amount_due`, `expiry_date`,
`challan_pdf_url`. The payer adds the identifier as a beneficiary and pays by
IMPS/NEFT/RTGS or at a branch; the merchant gets `ORDER_PROCESSED`. The "unique customer
identifier" is described as persistent per customer. An expired challan fails the order.
Not documented: over- or under-payment, or a payment after expiry [CHECK].

**Split Settlements** (`/split-settlements/*`). Split rules are set at order creation
(`split_info` → `split_details[]` with `split_merchant_id`, amount, `on_hold`); held splits
are released with `PATCH /api/pay/v1/orders/{orderId}/settlementId/{settlementId}/release`
(`release_amount`; partial release allowed) or cancelled. Split status `RELEASED|HOLD`. Not
supported on EMI or Pay-by-Points. Needs activation by support. Recipients are onboarded
split merchants [CHECK whether an individual claimant can be one].

**Settlements and reconciliation.** `GET /api/settlements/v1/list` (≤60-day range, 10 per
page, 6 months of history, "delay of up to 3 hours in rare cases"); Get Settlements by UTR
returns per-transaction lines plus refunds, chargeback recovery, **loan recovery**, MDR,
GST, split fund, platform fee. Setu **Reports API** (`/bifrost/collect/reports`) filters
by `platformBillStatus` incl. `SETTLEMENT_SUCCESSFUL`.

**Payment Links** (`POST /api/pay/v1/paymentlink`): `amount`, `expire_by` (≤180 days),
`allowed_payment_methods`, `merchant_payment_link_reference` (idempotency), customer
details; partial payments configurable; dashboard default cap ₹5,000 (`500000` paise,
configurable).

**Verify and validate.** Verify VPA (`POST /payment-option`, `fetch_vpa` by phone →
`fetched_vpa`; error `UPI_VPA_NOT_FOUND`). TPV (payments only from a registered account;
40+ banks net banking, 600+ banks UPI). Setu **Bank Account Verification** (₹1 penny drop,
sync/async) and **reverse penny drop** (customer pays ₹1 to a VPA; Setu returns their
account details by webhook; refunded in 24–48 h), plus **Name Match API**.

**Setu Account Aggregator (consent object).** Request: `consentDuration` or
`consentDateRange`; `consentMode` VIEW/STORE/QUERY/STREAM; **`fetchType` ONETIME/PERIODIC**;
`consentTypes` PROFILE/SUMMARY/TRANSACTIONS; `fiTypes` (DEPOSIT, **INSURANCE_POLICIES**,
MUTUAL_FUNDS, …); `vua` (mobile or mobile@aa); **`purpose`** 101–105 (**104 = "Explicit
consent to monitor the accounts"**); `dataRange`; `dataLife`; `frequency` (max 1/hour,
24/day); **`dataFilter`** (e.g. TRANSACTIONAMOUNT ≥ X); `context` incl.
**`transactionType: credit`**, `accounttype`, `fipId`, `purposeDescription`. Response: `id`,
`url`, `status`. Statuses: PENDING · ACTIVE · REJECTED · REVOKED · PAUSED · EXPIRED
(notification `CONSENT_STATUS_UPDATE`; rejection reasons such as `reject_not_want_to_share`).
**Only regulated entities (RBI/SEBI/IRDAI/PFRDA) can be FIUs** → our NBFC partner holds the
consent, not us. The `INSURANCE_POLICIES` FI type carries covers, cover amount, sub-limits,
conditions, exclusions, riders and policy dates, but **no claim data**. Which insurers are
live FIPs is a [CHECK].

**Setu Aadhaar eSign + eStamp.** Legally enforceable Aadhaar signatures (NSDL / eMudhra
infrastructure), **up to 6 signers per document**, signed-PDF download; statuses include
`sign_initiated`, `sign_in_progress`, `sign_pending`, `sign_complete`, per-signer `pending /
signed / failed / expired`. **eStamp** attaches a state stamp (`estampState`,
`estampValue`, `estampMergePosition`; stock acquired by request to support@setu.co).
eSign Name Match checks the signer name.

**Setu DigiLocker.** Pulls issuer-sourced documents with user consent ("at par with
original physical documents" under IT Rules 2016 r.9A). The integration guide shows
driving licence; whether insurance policies, health records or discharge summaries are
pullable is not stated [CHECK].

**Setu Insights / Signal IQ.** Insights include `quarterly/semi_yearly/yearly_salary_average`,
`inflows_monthly_summary`, `total_credits_value`, cheque bounces, EOD balances. Signal IQ
runs AA consent → fetch → insights as one flow with webhooks and a `reportId`.

**UPI Setu mandate statuses.** `mandate.initiated / live / rejected / paused / revoked /
completed`; revoke webhooks `mandate_operation.revoke.initiated / success / failed`. "A
single block multi debit mandate can only be revoked via merchant initiated collect flow."
UPI Setu API: `Idempotency-Key` on every POST (24 h), cursor pagination, webhooks signed
with `X-Setu-Signature` (HMAC-SHA256), retried for 24 h then quarantined.

**WhatsApp Collect** (Setu): collection reminders with an embedded payment link, sent from
our WhatsApp Business number via a partner BSP; templates in any language; ~5 days to
integrate, ~2 weeks to go live.

**Webhooks (Pine Labs Online).** Events: ORDER_AUTHORIZED / PROCESSED / CANCELLED / FAILED /
SETTLED / SETTLEMENT_REJECTED · PAYMENT_FAILED · REFUND_PROCESSED / FAILED · TOKEN_* ·
CUSTOMER_* · SUBSCRIPTION_* · `payout-transaction-success/failed`. Retries: immediately,
5 s, 5 min, 30 min, 2 h, 5 h, then 2 × 10 h; 2XX within 5 s required; out-of-order delivery
expected; URL set via support. Signature verification documented.

**Error codes** (full list `/developer-tools/error-codes/list`): e.g. `DUPLICATE_REQUEST`,
`AMOUNT_LIMIT_EXCEEDED`, `INSUFFICIENT_FUNDS`, `INVALID_USER_ACCOUNT`, `PAYMENT_EXPIRED`,
`API_RATE_LIMIT`, `PAYMENT_RATE_LIMIT`, `UNAUTHORIZED`, `ORDER_NOT_FOUND`,
`REFUND_DURATION_EXCEEDED`, `UPI_VPA_NOT_FOUND`.

#### What a "permission" looks like on this rail
Four distinct objects, each held by a different party:
1. **Debit mandate** (AutoPay/eNACH/OTM/ReservePay): payer → merchant; max amount,
   frequency, validity; revocable by the customer except OTM/SBMD (merchant-only revoke) and
   the "non-revocable" AutoPay option [CHECK].
2. **Grantex grant** (via P3P): human → agent; scopes, per-transaction cap, budget, expiry,
   purpose; revocable; JWT, verifiable offline.
3. **AA consent**: human → regulated FIU; data types, purpose code, duration, frequency,
   filters; the human can pause or revoke.
4. **eSigned document**: any legal instrument (e.g. a deed of assignment), up to 6 signers,
   optionally stamped. The rail signs it; it does not enforce it.

#### Sandbox and test access
- Pine Labs Online: free sign-up at https://dashboardv2.pluralonline.com/signup → Test mode
  → Settings → API Keys (client id/secret); UAT base `https://pluraluat.v2.pinepg.in`; test
  cards page; Postman collection; CLI `pinelabs` with `listen/trigger` for webhooks.
  Webhook URLs are configured by contacting support. P3P needs Pine Labs onboarding plus a
  Grantex account.
- Setu: sign up on The Bridge (https://bridge.setu.co/v2/signup); sandbox keys are
  pre-seeded; UPI Setu sandbox `https://uat.setu.co` ("simulated bank rails"); AA has a mock
  FIP (`setu-fip`). Reverse penny drop and WhatsApp Collect need sales/KYC onboarding.

#### Anything agentic
- **P3P** (above) and **Grantex** (third party).
- **Pine Labs MCP Server** (hosted "API Execution" or local `pinelabs-mcp` CLI): 30+ tools,
  namely Orders (3), Checkout (1), Payment Links (5), **Subscriptions (22** incl.
  `create_presentation`, `send_subscription_notification`, `create_debit`,
  `create_merchant_retry`), UPI (1). **No payout, refund, settlement or split tools.**
- **Agent Enablement Toolkit** `@plural_pinelabs/agent-toolkit` (OpenAI Agents SDK,
  LangChain, Vercel AI SDK): only `createOrder`, `getOrder`, `cancelOrder`, `createRefund`.
- **Agent Skills** (coding-assistant guidance) · **Pine Labs CLI** (idempotency keys on
  every write, audit log at `~/.pinelabs/audit.log`, an MCP-backed `ask` planner that
  "cannot run payments directly" and prompts before any non-read-only action).
- **Agentic Commerce Suite** (`/ai/agentic-commerce`): "Pine Labs × OpenAI"; checkout inside
  ChatGPT "live today on India's UPI rails"; "Claude and Gemini next". Pillars include
  "Reasoning-Led Credit… Predictive recovery agents in collections" (marketing, no API).
  Press: "Pine Labs Collaborates with OpenAI" (19 Feb 2026).
- **Setu agentic bill payments** on Claude and ChatGPT (10 Dec 2025): fetches bills, flags
  anomalies, pays "on simple rules defined by the consumer, ensuring it never initiates an
  incorrect payment or exceeds preset limits". **MCP Server for Bill Payments** tools: List
  Billers, List Categories, Get Saved Bills, Fetch Bill, Pay Bill, Check Payment Status, Get
  Transaction Receipt, List Payment History.
- Setu **Sesame** BFSI LLM (with Sarvam AI, May 2024).

#### Candidate Q4 rows: Pine Labs (Used at = blank until Q3 is locked)

| Name | Used at | Rail | What you send it | What comes back | When it fails | What it must never do | What exists today | Build status |
|---|---|---|---|---|---|---|---|---|
| `verify_claimant_account` | | Payments (Setu) | claimant bank a/c + IFSC (or ₹1 reverse-penny-drop link), name | account valid/holder name; name-match score | a/c invalid/closed, name mismatch → stop, ask claimant | pay to an account whose holder isn't the claimant | Setu "Bank Account Verification" (penny drop), "Reverse penny drop", "Name Match API" (docs.setu.co/data/bav, /data/match-apis); Pine Labs "Verify VPA" `/api/payment-option` | EXISTS |
| `kyc_claimant` | | Payments (Setu) | PAN / Aadhaar OTP / DigiLocker consent | verified identity fields | mismatch, OTP failure | proceed on unverified identity | Setu KYC, PAN, Aadhaar-lite, DigiLocker (docs.setu.co/data/kyc) | EXISTS |
| `sign_claim_assignment` | | Payments (Setu) | assignment deed PDF, signer list (claimant; optionally employer signatory), stamp state/value | signature request id, per-signer status, signed PDF | signer abandons/expires, name mismatch | treat a signature as consent to anything beyond the deed's named claim | Setu "Aadhaar eSign" + "eStamp" (docs.setu.co/data/esign, /data/esign/estamp) | EXISTS (signing); legal effect OFF-RAIL [CHECK TPA s.130] |
| `grant_agent_authority` | | Payments (P3P/Grantex) | principal, agent id, scopes, purpose, caps, expiry | grant token (JWT), grant id; revocation events | consent refused/expired/revoked → stop acting | act outside the named purpose/claim | "Grantex" via P3P docs (/ai/p3p/sdks; docs.grantex.dev purpose-bound grants) | PARTIAL (third-party; built for payments) |
| `check_float_balance` | | Payments | — | funding a/c balance | no funding a/c linked; below threshold | disburse against a balance it hasn't checked | "Get Payout Balance" `/payouts/v3/payments/funding-account` | EXISTS |
| `disburse_advance` | | Payments | claim id as `clientReferenceId`, payee, verified a/c or VPA, amount, mode, remarks | 201; status SCHEDULED→…→SUCCESS/FAILED; UTR; webhook | FAILED w/ message (e.g. account frozen), 409, funding short → retry once on same key, then escalate | pay twice for one claim; exceed the approved advance or ₹10 lakh | "Create Payout API" `POST /payouts/v3/payments/banks`; webhooks `payout-transaction-*` | EXISTS |
| `confirm_disbursal` | | Payments | `clientReferenceId` or UTR | status, UTR, fees, tax, timestamps | not found / PENDING past SLA | report "paid" before SUCCESS + UTR | "List Payouts API" `GET /payouts/v3/payments` | EXISTS |
| `register_recovery_mandate` | | Payments | plan (`AS`, `max_limit_amount`), customer, TPV bank a/c = salary a/c | subscription id, status ACTIVE…; SUBSCRIPTION_* webhooks | EXPIRED (4 h), INACTIVE, REVOKE; customer revokes later | debit anything but the named claim's shortfall | Subscriptions API `/ps/api/v1/public/subscriptions`, "Non Revocable Mandate Setup" [CHECK] | EXISTS (pull fallback) |
| `collect_recovery_debit` | | Payments | subscription id, amount = amount owed on that claim | PDN NOTIFIED → debit COMPLETED/FAILED; SUBSCRIPTION_CHARGED | FAILED ×3 → HALTED → human | debit before the payout has landed with the claimant; skip the ≥24 h pre-debit notice | "Subscription Notification", "Create Debit", "Create Merchant Retry" | EXISTS |
| `issue_claim_collection_account` | | Payments | order for the claim amount | `virtual_account_id`, IFSC, bank, expiry, challan PDF; ORDER_PROCESSED | expiry; payer ignores it | present itself as the claimant's own account | "Bank Transfer / ECMS" Create Challan `/api/pay/v1/order/{id}/challan` | PARTIAL (payer must choose to pay it; order-bound, expires) |
| `watch_for_payout_landing` | | Payments (Setu AA) | consent: PERIODIC, purpose 104, DEPOSIT, `transactionType` credit, amount filter, claimant's salary a/c | periodic transactions; consent status | consent REJECTED/REVOKED/PAUSED/EXPIRED → fall back to asking the claimant | read beyond the consented account/filter; be used for anything but this claim | Setu "Account Aggregator" consent object (docs.setu.co/data/account-aggregator/consent-object) | EXISTS (only via a regulated FIU, our NBFC partner) |
| `send_recovery_link` | | Payments | amount owed, claimant, expiry (≤180 d), idempotency ref | link URL, status | expired/unpaid | chase for more than is owed | "Payment Links" `/api/pay/v1/paymentlink`; Setu "WhatsApp Collect" reminders | EXISTS |
| `split_recovery` | | Payments | recovery order with `split_info` (lender share, claimant residual on hold) | split ids; RELEASED/HOLD | only for pay-ins through our own Pine Labs order | release the residual before the ledger reconciles | "Split Settlements", "Release Settlement" | PARTIAL |
| `reconcile_to_rupee` | | Payments | date range / UTRs / claim ids | settlements w/ deductions, per-txn lines; payout UTRs | ≤60-day window, 10/page, ≤3 h lag | close a ledger with an unexplained paisa | "Get All Settlements", "Get Settlements by UTR", "List Payouts API"; Setu "Reports API" | EXISTS |
| `read_policy_terms` | | Payments (Setu AA) | AA consent, fiTypes INSURANCE_POLICIES | covers, sub-limits, conditions, exclusions | insurer not a live FIP [CHECK] | treat policy terms as claim status | AA FI data types (docs.setu.co/data/account-aggregator/fi-data-types) | PARTIAL |
| `underwrite_from_bank_data` | | Payments (Setu) | AA consent / statement PDF | salary averages, inflows, bounces | no consent; thin data | use data beyond the consented purpose | "Setu Insights", "Signal IQ" | EXISTS (via FIU) |
| `assign_inbound_payment` | | Payments | claimant's signed instruction naming one reimbursement, payer, amount, destination a/c | payer-side acknowledgement; routed credit | payer refuses/ignores; claimant revokes | route any payment other than the named claim | nothing: no payee-side object on the rail | MUST BUILD |

#### Gaps (what we need that this rail does not have → MUST BUILD rows and Q5)
1. **No payee-side assignment or redirect object.** Nothing lets the claimant bind their
   employer or insurer to pay us. It remains the core must-build (`assign_inbound_payment`).
2. **Virtual accounts only work if the payer co-operates.** ECMS is order-bound and
   expiring, and only receives money that the employer chooses to send there.
3. **Split settlement only splits money that passes through our own Pine Labs checkout.**
   It cannot split an employer's NEFT to the claimant's salary account.
4. **Recovery is a pull after the fact**: AutoPay/eNACH on the claimant, revocable
   (non-revocable option [CHECK]), with ≥24 h pre-debit notice; OTM ≤₹1 lakh / 60 days;
   Reserve Pay ≤₹10,000.
5. **No lending product.** The advance is a payout from our own funded account; the licence
   (co-lending/NBFC) is off-rail. "Reasoning-Led Credit" is marketing with no API.
6. **No claim-state data anywhere**: nothing about whether an employer or insurer has
   received, approved or scheduled a claim. The AA insurance type has policy terms only.
7. **The agent tooling is thin for our job**: the MCP server and Agent Toolkit have no
   payouts, settlements, splits or refunds; the agent calls REST directly.
8. **AA consent needs a regulated FIU** (our NBFC partner), and hourly fetches at most.
9. **P3P/Grantex authority covers spending only**; nothing expresses "act in my name
   towards a third party" [CHECK Grantex custom purposes].

#### Surprises (useful things we weren't looking for)
- **Setu is Pine Labs.** So AA, Aadhaar eSign + eStamp, BAV, DigiLocker, UPI mandates, BBPS
  and WhatsApp Collect are all on the Pine Labs rail. The "consented-data rail" we listed as
  a Q5 candidate is already partly inside rail 1.
- **AA monitoring can see the payout land.** With purpose 104, PERIODIC fetch and a credit
  filter, the agent can detect the employer's reimbursement credit in the claimant's account
  and trigger recovery without asking anyone.
- **eSign with up to 6 signers** means one document can carry the claimant's assignment
  *and* the employer's acknowledgement (the notice to the debtor that TPA s.130 needs
  [CHECK law]), with state stamp duty applied through eStamp.
- **Grantex evidence packages** (hash-chained, signed, verifiable offline) are a ready format
  for a tamper-evident claim file: grant, every call, every human decision.
- **Setu already runs a bounded money-moving agent on Claude and ChatGPT** (bill payments,
  consumer-set limits). This is the closest Indian precedent for our L3 money acts, and
  relevant to Q8.
- **Pine Labs runs a corporate expense platform** ("Manage corporate expenses": spend
  policies, approval hierarchies, "Automate reimbursements, ledger sync and monthly caps",
  ERP/HRMS integration, prepaid travel/meal cards;
  https://www.pinelabs.com/use-cases/manage-corporate-expenses). Pine Labs sits inside some
  employers' reimbursement flow, which makes it a candidate claim-state source (Q5) and a
  Q8 contender. There are no API docs for it [CHECK].
- The settlement report has a `total_loan_recovery_amount` field (deduct-at-source on
  merchant settlements) [CHECK what product it serves].
- The health-industry page claims "Insurance integration — Streamlined insurance claim
  processing", but it links only to the generic Fintech Infrastructure page. No product or
  API sits behind it.

### 10.2 Gnani (voice)

**Where the docs are.** https://docs.gnani.ai/ (index `/llms.txt`, full text `/llms-full.txt`; every
page is also served as Markdown by appending `.md`; `/sitemap.xml` lists no pages beyond llms.txt).
The OpenAPI/AsyncAPI files that llms.txt links (`/agent_config_openapi.yml`, `/STT.yml`, etc.) all
return **404** (checked 24 Sep 2026). Each API page carries its own OpenAPI block instead, and the
Platform API intro embeds a Postman collection ("Gnani Agent Builder Platform API"). Pages say
"Last verified" 5–11 Aug 2026. The docs cover three layers, each with its own host and key:
- **Gnani Speech APIs:** base `https://api.vachana.ai`, header `X-API-Key-ID`; keys generated at
  https://app.gnani.ai/voice. Models: **Gnani Prisma v2.5** (STT), **Gnani Timbre v2.5** (TTS; v2.0
  deprecated), `vachana-vc-v1` (voice cloning).
- **Agent Builder** (the console at https://app.gnani.ai/; the docs also call it "Gnani Agents"):
  no-code voice agents with knowledge base, actions, integrations, logs and analytics.
- **Agent Builder Platform API:** base `https://api.inya.ai/platform`, header `x-api-key`; keys are
  scoped by permission **`agents`** (`/v1/agents/*`) or **`conversations`** (`/v1/conversations/*`)
  (401 = bad key, 403 = missing permission). Spec title "Platform Agents API", v2.1.0. Envelope
  `{status, requestId, message, response}`.
- "Inya" is the internal/product name behind the agent layer: host `api.inya.ai`, the payload key
  `inya_data`, the Webex widget `INYA_TRANSCRIPT`, and the contact address `hello-inya@gnani.site`.

**Platform not yet explored.** https://app.gnani.ai/ could not be opened this session (the browser
tool was locked by another session). Everything below comes from the docs and the public
gnani.ai site. Items only the platform can settle are tagged **[CHECK platform]**.

#### Full product and API list (exact names)
- **Speech-to-Text (Prisma v2.5):** **Speech-to-Text (REST)** `POST /stt/v3` (/api/STT/speech-to-text)
  · **Speech-to-Text (Realtime)** `wss://api.vachana.ai/stt/v3/stream` (/api/STT/stt-websocket) ·
  **Batch STT**: Create Job `POST /stt/v3/batch/jobs`, Start Job `…/{job_id}/start`, Get Job Status
  `GET …/{job_id}`, List Jobs `GET /stt/v3/batch/jobs`, Get Job Files `GET …/{job_id}/files`, Cancel
  Job `POST …/{job_id}/cancel` (/api/STTBatch/*).
- **Text-to-Speech (Timbre v2.5):** **Text-to-Speech (REST)** `POST /api/v1/tts/inference` ·
  **Text-to-Speech (Streaming)** SSE `POST /api/v1/tts/sse` · **Text-to-Speech (Realtime)**
  `wss://api.vachana.ai/api/v1/tts` · **Available Voices** · **Text Normalization Guide**
  (/api/TTS/*).
- **Voice cloning:** **Voice Clone Embeddings** `POST /api/v1/tts/voice-clone/embeddings` · **Voice
  Cloned TTS** REST / Streaming / Realtime (same TTS endpoints with `speaker_embedding`) (/api/VC/*).
- **SDKs and plugins:** **Python SDK** `gnani-vachana` (Python 3.10+; `GnaniSTTClient`,
  `GnaniSTTStreamClient`, TTS clients) · **LiveKit Plugin** `livekit-plugins-gnani` · **Pipecat
  Plugin** `pipecat-gnani` (tested with Pipecat v1.5.0).
- **Use-case guides:** Podcast Transcription with Speaker Labels · **Call Analytics Pipeline** (Batch
  STT + Claude or OpenAI) · **Real-Time Quality & Compliance Monitoring** (/api/use-cases/*).
- **Agent Builder guides:** Creating a Knowledge Base (/A01_KB) · Creating Your First Agent
  (/A02_Agent) · Testing Your Agent (/A03_Testing) · Whitelisting Numbers (/A04_Whitelisting) ·
  **Creating a Workforce** (/creating-a-workforce) · **DTMF Collection** (/B01_DTMF) · Advanced ASR
  Settings (/B02_Advanced_ASR) · **Voicemail Detection** (/B03_Voicemail) · **Dynamic Variables &
  Dynamic Messages** (/B04_Dynamic_Variables) · **Writing a Disposition Prompt** (/C01_Disposition) ·
  Language Switch Prompt (/C02_Language_Switch) · Using Jinja for Dynamic System Prompts (/C03_Jinja)
  · SMS Integration and Action (Twilio, /D01_Twilio_SMS) · CRM Integration and Action (Zoho CRM,
  /D02_Zoho_CRM) · Email Integration and Action (Mailchimp or SendGrid, /D03_MailSend_Email) ·
  Ticketing Integration and Actions (Zoho Desk, /D04_Zoho_Ticket) · **Custom Integrations and
  Actions** (/D05_Custom) · Integrating Gnani Agents with Webex Contact Center (/D06_Webex) ·
  **Conversational Logs** (/E01_Conversational_Logs) · Dev Logs (/E02_Dev_Logs) · Agent Analytics
  (/E03_Agent_Analytics) · Action Logs (/E04_Action_Logs) · Organizations (/F02_Org) · Environments
  (/F03_Env) · Need Help? (/F01_Support) · Setting Up Integrations (/M03_Integrations) · Managing
  Variables & Actions (/M04_Actions) · **Agent Chaining** (/M05_Chains) · Dynamic Variables & Prompt
  Validation (/M10_Dynamic_Variables) · **Import Twilio number** (/M16x_Import_Number) · Dashboard
  (/M21_Dashboard).
- **Platform API (/Platform/*):** Agents: Create Agent `POST /v1/agents` · List Agents `GET /v1/agents`
  · Get Agent / Update Agent / Delete Agent `GET|PUT|DELETE /v1/agents/{botId}` · **Trigger Test
  Call** `POST /v1/agents/{botId}/trigger_call` · Validate Prompt `POST /v1/agents/prompt/validate`.
  Agent config: Get Languages, Get Regions, Get Timezones, Get LLM Models, Get Transcriber Config,
  Get TTS Config (`/v1/agents/config/...`). FAQ: Add FAQ Entries, List FAQs, Update FAQ, Delete FAQs,
  Get FAQ Sample, Bulk Import FAQs (`/v1/agents/{botId}/faqs[...]`). Conversations: **Get
  Conversation Logs** `POST /v1/conversations/logs` · **Get Conversation Statistics** `GET
  /v1/conversations/{conversationId}/stats` · **Get Conversation Audio** `GET
  /v1/conversations/{conversationId}/audio`. Chat SDK: Get/Update Chat Widget Config, Upload Chat
  Widget Icon. **Post-call webhook** (configured through Update Agent). Error Reference.
- **Marketing-site products with no API docs** (https://www.gnani.ai/): **Biometrics**
  (/dev/products/biometrics), **Analytics / "Aura365"** (/dev/products/analytics), **Assist**
  (/dev/products/assist; "sub-500ms hints, compliance prompts, next-best-action"), **Agents**
  (/dev/products/agents; a "Banking Collections Agent" in Hindi and a "Neo Service Booking Agent"
  are shown), models **Gnani Warp v2.0** (speech-to-speech), **Gnani Evon v3.3** (LLM; "BFSI,
  insurance, healthcare"), **Gnani Aion v3.2** (#1 on BFCL v3 function calling, per the site),
  **Gnani Artha** ("India's sovereign AI stack"). Pricing: https://www.gnani.ai/pricing redirects to
  /book-demo. No public price list.

#### The questions to settle, answered from the docs

**1. Outbound vs inbound, and how an outbound call is triggered in production.**
- The only documented API that places a call is **Trigger Test Call**. It "only work[s] to
  **whitelisted phone numbers**. Calling an unregistered number returns HTTP `400`" (`"Phone
  number is not registered for outbound calls"`), and it "is for testing — not large-scale
  production campaigns." Keys with the Developer role can call only in `environment=development`
  (403 `"Developer can only trigger calls in the development environment"`). Whitelisting is
  per number: Phone Numbers → Whitelisted → Add Number → **OTP** to that phone. The API page says to
  "Contact your account manager to register numbers."
- **No campaign or bulk-dial API exists in the docs.** Dynamic Messages page: "Currently, Gnani
  Agents does **not** have a built-in campaign manager. This feature is available only by contacting
  us to enable it for your deployed bot. We're working to make it self-service soon."
- **Going live is done by Gnani.** "Deployment to live infrastructure is handled by the Gnani Agents
  team. An agent must be in Production before deployment can be requested" (Organizations,
  Environments). Organizations themselves are created only by Gnani on request.
- **Outbound is the default shape.** Workforce: "every workforce begins with an Outbound Call
  Trigger." Voicemail detection is an outbound feature. The worked examples are collections calls
  (Muthoot Capital EMI reminder; the `PTP` / `RTP` codes).
- **Inbound exists but is thinly documented.** The webhook `bot_type` is `voice_outbound` or
  `voice_inbound`; Import Twilio number lets you "assign numbers to agents for inbound or outbound
  calls"; Agent Chaining config includes "agent phone numbers"; the Webex Contact Center
  integration puts Gnani agents into Cisco Flow Designer. No doc covers inbound routing, an Indian
  (non-Twilio) number, or whether Gnani provides numbers [CHECK platform].
- `clientReferenceId` (optional, free-form) on Trigger Call is stored on the conversation, sent to
  the dynamic greeting API, and "may appear" in the post-call webhook. It is the only per-call
  correlation key we send.

**2. Supported Indian languages (the lists differ by layer).**
- **STT REST and Realtime (Prisma v2.5): 10.** Bengali `bn-IN`, English `en-IN` (accepts English-Hindi
  mixed audio), Gujarati `gu-IN`, Hindi `hi-IN`, Kannada `kn-IN`, Malayalam `ml-IN`, Marathi `mr-IN`,
  Punjabi `pa-IN`, Tamil `ta-IN`, Telugu `te-IN`.
- **Batch STT: 8.** The same list minus Gujarati and Punjabi. The Batch page table and the
  `UNSUPPORTED_LANGUAGE` error both list 8, although the REST page says "the nine languages listed
  on the Batch introduction page". Up to 3 comma-separated codes enable per-file language
  identification.
- **TTS (Timbre v2.5): the same 10, plus `hi-en` (Hinglish) and `auto`**, with 42 voices (for
  example Hindi: Nalini, Bhavna, Yashvi, Urmila, Jwala, Chitra, Ambuja, Deepak, Roopesh, Vikrant,
  Hemraj, Jalaj, Omkar; Tamil 5, Telugu 5, English 6, 2 each for kn/ml/mr/bn/gu/pa).
- **Voice agents (Agent Builder): narrower, and only examples are published.** Get Languages
  example: en-IN, hi-IN, ta-IN, te-IN, kn-IN with allowed pairings; "The supported language list
  grows over time. Always fetch this endpoint." **Max 3 languages per agent.** ASR examples: `gnani`
  models `gnani_vachana_rest` / `gnani_v2` ("Vachana") cover hi, en, te, ta, mr, bn, kn, ml;
  Microsoft `microsoft_rest` / `microsoft_streaming` cover en-IN, hi-IN, en-US, ta-IN, te-IN. TTS
  config example (provider `vachana_timbre-v2.5`) covers en, hi, kn, ta, te. LLM examples list
  en-IN, hi-IN, ta-IN, kn-IN, en-US. The live language list for agents is a [CHECK platform].
- Mid-call switching: `languageSwitch`, `languageSwitchMode` `implicit|explicit`,
  `minWordsForLangSwitch` (default 2) plus a Language Switch Prompt that reads three STT engine
  outputs. Each user turn in Stats carries `totalResults` (a transcript per configured language) and
  `detectedLanguage`.
- Marketing claims "40+ languages" (models) and Timbre "21+ languages". Neither matches the API docs.

**3. Can an agent navigate a counterparty's IVR (send DTMF)? No, not per the docs.**
DTMF is **collection only**: the toggle Agent Settings → Customize → DTMF Collection
(`advanceSettings.enableDtmf`), plus a prompt signal `| DTMF[XXYY]` (XX = digits expected, YY =
seconds; e.g. `| DTMF1010` for a 10-digit phone number, `| DTMF0610` for a 6-digit PIN code). No
field, action or event sends tones, and nothing detects or navigates a menu. The ITN/VAD docs mention
IVR only as a style of short-command audio. So an outbound agent calling a TPA or insurer helpline
that opens with "press 1…" cannot get through on its own → MUST BUILD / OFF-RAIL.

**4. Summaries, dispositions and structured extraction: yes, and it is the strongest part.**
- **Call Dispositions** (agent → Analytics Config tab): a default prompt plus named dispositions,
  each with its own prompt. The documented template makes the LLM output **strict JSON with our own
  field definitions and allowed values** (e.g. `STAGE_CODE`, plus any keys we define). Assigned
  "automatically after each call".
- Output fields: `overallCallDisposition` (Stats; standard codes `PTP` Promise to Pay, `RTP` Refused
  to Pay, `AP` Already Paid, `CLBK` Callback Requested, `WRNG` Wrong Number, `DSCN` Call
  Disconnected, `RNR` No Answer, `DND` Do Not Disturb; custom codes allowed, "treat unknown values
  as opaque strings") · `callSummary.disposition` (LLM label, may be `null` until analytics finish)
  · webhook `STAGE_CODE`, **`disposition_result`** and **`post_call_extraction_v2`** ("Structured
  disposition extraction… Fields depend on your disposition configuration"; the example carries
  `ptp_date`, `clbk_date`, `clbk_time`, `language_captured`).
- Conversational Logs show "**Call Insights**: summarized details on the call's reason, result,
  overview, and resolution". Agent Analytics shows sentiment trend, top reasons, intents, topics,
  dispositions, actions triggered and drop-off rate. Whether these insight fields are exposed by API
  is not documented [CHECK platform].
- In-call capture: **Variables** (Boolean/Integer/Float/String, each with a prompt such as "Ask the
  user for their PIN code (must be 6 digits)") feed On-Call actions ("Before API Call Variables" sent
  out, "After API Call Variables" received) and Post-Call actions. The docs mark "Store API
  responses" as "(Coming Soon)" on the Variables page, but "After API Call Variables (received from
  the API)" on every action page [CHECK which holds]. Workforce handoffs pass "Structured data
  extracted during the call".

**5. Voice authentication / biometrics: exists as a product, not in the docs.**
No API or Agent Builder page mentions it. The marketing page https://www.gnani.ai/dev/products/biometrics:
"Authenticate callers in <5s with 300+ acoustic features", "Encrypted voiceprint", "Cross-lingual —
enrol in one language, verify in any other", SIP/SIPREC; the homepage adds "Passive voice biometrics…
Anti-spoof and liveness detection built in." Access, API and pricing are [CHECK] (likely enterprise,
via demo). The documented alternative is DTMF collection of a PIN/OTP that we verify ourselves
through an On-Call custom action.

**6. Recordings and transcripts: retrievable, but not evidence-grade.**
- **Get Conversation Statistics** gives `conversationId`, `botId`, `startTime`/`endTime` (Unix s),
  `callStatus` (`ANSWERED`, `NO ANSWER`, …), `callDuration` (0 if unanswered),
  `overallCallDisposition`, `callSummary`, **`utteranceAnalytics`** (turns: `role`
  assistant/user, `content`, **`timestamp`** Unix seconds with fractions, and on user turns
  `detectedLanguage`, `totalResults`, `userInterruptionFlag`), `averageAgentLatency`,
  `callProcessed`, `lastProcessedOn`. 404 `"Conversation not found"`.
- **Get Conversation Audio** returns `audio/mpeg` (MP3). 404 `"Audio file not found at path: …"`
  when "Recording disabled for agent", the "call too short to record", or the file is not yet
  available. Use GET, since HEAD may 405. The existence of a per-agent recording setting is implied
  here, but no documented field controls it [CHECK platform].
- **Get Conversation Logs**: POST search with `pageNo`, `pageSize` (≤100 recommended),
  `searchTerm` (name, keyword or `conversationId`), `filter.startDate/endDate` (ISO 8601),
  `filter.callStatus`, `filter.botId`; `transcript` in the list is "often empty or partial".
- The **webhook's `call_infra.call_status`** is a telephony CDR: `callStartTime`,
  `callConnectedTime`, `callEndTime` (e.g. "2026/08/11 16:35:01 +0000"), `ringingTime`,
  `setupTime`, `gnanivb_billing_duration`, `srcPhone` (the caller ID used, e.g. +9180…),
  `dstPhone`, `callType` "Outbound", `rec_path`.
- **Evidence limits:** no retention period is documented for recordings or transcripts (the
  gnani.ai privacy policy covers website users, not call data) [CHECK]. There is no hash, signature
  or content digest on recordings, transcripts or webhooks, and webhook auth is only the static
  headers we configure. "Audit logs" are listed under "Current Limitations… coming soon", and there
  is no version history for agent config (overwrite model). Batch `transcript_url` is a presigned S3
  URL that expires in 1 hour. To use a call in an appeal, we must pull audio + transcript + CDR
  immediately and seal them ourselves (hash, trusted timestamp, our own store) → OFF-RAIL.

**7. Consent and recording disclosure: nothing built in.**
The only text: "Ensure you have proper consent and comply with local telecommunications regulations
before triggering outbound calls" (Trigger Test Call). There is no consent field, no disclosure
setting and no consent capture event. A disclosure has to be written into the greeting/system
prompt, and its delivery checked from the transcript. The **Real-Time Compliance** guide shows
exactly this pattern as customer-side code (a `required_disclosures` rule matching "this call is
being recorded" within the first 3 segments over the realtime STT stream). The `DND` disposition
code exists for opt-outs, but suppression lists and calling-hour rules are not documented.

**8. Webhooks and callbacks.**
- **Post-call webhook:** Update Agent `hasPostCallTrigger: true` + `postCallTriggerAPIConfig
  {hasHeaders, method GET|POST, url, headers[{id,key,value}]}`. It fires "after every call ends",
  snake_case payload (`conversation_id`, `bot_id`, `bot_type`, `environment`, `call_type`,
  `organization_id`, `phone`, `user_context`, `callStatus`, `STAGE_CODE`, `disposition_result`,
  `post_call_extraction_v2`, `transcript` / duplicate `conversation_log`, `call_infra`,
  `rec_path`). "The same call may be delivered more than once": key on `conversation_id`, return
  2xx fast. No retry schedule, timeout or signature is documented.
- **Pre-call hook, Dynamic Messages:** before the call Gnani sends `{conversation_id, mobile}` to our
  URL (GET/POST + headers); we return `additional_info.inya_data.text` (the greeting) and
  `user_context` (variables). **10-second timeout, after which "the call will fail"**; returning 200
  places the call, returning 400 stops it. So our system can veto every call at the last moment.
- **Actions** (custom HTTP GET/POST/PUT/DELETE, per-action timeout; triggers **On-Call** with a
  "Speak During Action" line, or **Post-Call**). Voicemail **Post Detection Actions** (SMS, email,
  custom API). Every action execution is visible in **Action Logs** (time, payload, response, status
  code).
- **Batch STT `callback_url`**: `job.completed`, `job.partial_failure`, `job.failed`,
  `job.cancelled`, with full transcripts; "Treat webhooks as best-effort. Polling remains the source
  of truth."

**9. Limits, errors, pricing and credits.**
- Platform API errors: 400, 401, 403, 404, 409, **429 (no number given; exponential backoff)**,
  500. Named messages include `Maximum 3 languages are allowed`, `Selected ASR model does not support
  selected languages…`, `QA role does not have permission to create/update agents`, `Agent not found
  or does not belong to your organization`, `Conversation not found`, `Audio file not found at
  path: …`. Validate Prompt returns 200 even for invalid Jinja (`isValidTemplate: false`) and for a
  missing `systemPrompt`. `pageNo=0` → 500 on List Agents, empty on Logs.
- Agent limits: 3 languages/agent · FAQs 100 per agent per environment, 10 phrasings each (import
  silently trims) · `maxTokens` 1–4096, temperature 0–1 · `maxSpeechDuration` 1–240 s ·
  voicemail message ≤300 chars, detection attempts 1–5, playback delay 1–10 s ("doesn't guarantee
  100% voicemail detection") · dynamic API 10 s · shareable browser-test link valid 5 minutes ·
  custom vocabulary `phraseConfig.phrase` ≤100 (only some ASR models).
- Speech limits: STT REST ≤60 s audio (ideal ≤30 s), 8–44.1 kHz · Realtime: 1,024-byte PCM
  frames at real-time cadence, 8/16/44.1/48 kHz, **session capped at 15 minutes**, VAD headers
  fixed per connection · Batch: ≤4 h per file, 100 files/job and 10 MB/file on upload (cloud URLs
  uncapped in size/count, 30-min download), ZIP 50 MB/200 MB, **diarisation max 2 speakers**, no ITN
  on batch, `transcript_url` 1 h, poll ≥10 s, "billing is per audio duration" · TTS speed
  0.85–1.15, telephony output `mulaw`/`alaw` at 8 kHz · voice-clone reference audio 5–30 s.
- Speech API errors: 400, **403 "Check your API key, organization status, or available credits"**,
  429 `RATE_LIMIT_ERROR`, 500, 503; Batch `MISSING_API_KEY`, `UNSUPPORTED_LANGUAGE`,
  `JOB_NOT_FOUND`, `AUDIO_TOO_LONG`, "Empty transcript after 3 retries".
- **Pricing:** none in the docs or on the public site. It is credit-based: the Dev Logs line "ORCH:
  Finalizing total call credits", the 403 "available credits", and Webex "credit setup" handled by
  Gnani. The organisers say sign-up comes with free credits. Rates per minute/call are [CHECK
  platform].

**10. Anything agentic, including LLM choice.**
- **LLM choice per agent** (`llmParams {provider, model, temperature, maxTokens}`). Get LLM Models
  example: **Anthropic `claude-3-5-sonnet-20241022`**, Gnani **"Pampa Go" / "Pampa Priority"**
  (default "Pampa Go"), OpenAI `gpt-4.1-mini`, `gpt-4o-mini`; each flagged `functionCalling: true`
  with its own `supportedLanguages`. The live list (and whether newer Claude models are offered) is
  [CHECK platform]. ASR providers include `gnani`, `microsoft`, and model ids for `elevenlabs_*`,
  `gladia_streaming` and `gemini-2.5-flash-native-audio-preview-09-2025`.
- **Tool use inside calls** = Actions (custom HTTP On-Call, with a spoken line while waiting) +
  Variables. **Agent Chaining** (Default / User / Decision / Event nodes; Event = End Call, Reset or
  **Transfer**; build from scratch, from a prompt, or by JSON import). **Workforce** (multi-agent
  canvas, natural-language handoff conditions, full context passed). **Call transfer** to a human
  number (`callTransferConfig`). **Validate Prompt** returns a Jinja check plus a `kvCache`
  optimisation score.
- **No MCP server for agents or calls** is documented. (The docs site answers at
  `https://docs.gnani.ai/mcp` with a JSON-RPC error. It looks like a docs-search MCP endpoint, not
  a platform API [CHECK].)
- Build-your-own path: STT/TTS through the **LiveKit** and **Pipecat** plugins, with any LLM (the
  Pipecat example uses Groq). The **Call Analytics Pipeline** guide runs Batch STT → **Claude**
  (`anthropic` SDK, `claude-opus-4-8`) or OpenAI for structured call analysis.

#### What a "permission" looks like on this rail
Nothing on this rail represents a counterparty's or claimant's permission. The objects that exist:
1. **API key + permission scope** (`agents` / `conversations`) and **org role** (Org Admin /
   Developer / QA, fixed permissions). Developer keys can only call in development.
2. **Whitelisted number**: an OTP-verified phone that test calls may dial. This is the account
   holder's own number, not consent from the person called.
3. **Environment gate**: Development → Staging (QA "Mark Ready for Production") → Production (Org
   Admin "Push to Production") → Gnani deploys. No rollback.
4. **Pre-call veto**: our Dynamic Messages API returns 200 or 400 per call. This is where our own
   mandate/consent check would sit.
5. **In-call spoken confirmation + DTMF**: an explicit "yes" or keypad entry, captured in the
   transcript/variables and the disposition JSON. This is evidence we create; the rail doesn't
   certify it.
Recording consent, DND/opt-out lists, calling-hour windows and the claimant's signed mandate (the
Setu eSign object from §10.1) all live in our system.

#### Sandbox and test access
- Sign up at https://app.gnani.ai/ (the organisers promise free credits). Speech API keys at
  https://app.gnani.ai/voice. TTS playground at https://app.gnani.ai/voice/text-to-speech. Docs
  "Try it" panels run live Batch STT calls.
- Agent testing in the console: **Test → Chat Window**, **Web-based (Voice)** (plus a shareable link
  valid 5 minutes), **Trigger Agent Call** to a whitelisted number. Platform API test flow: Create
  Agent → Update Agent → Trigger Test Call (`?environment=development`) → Logs → Stats / webhook.
  Postman collection embedded in /Platform/platform-introduction.
- Needs Gnani contact: Organizations, production deployment, the campaign manager, registering
  non-whitelisted numbers, Webex credit setup. Own numbers: Import Twilio number (Account SID + Auth
  Token). Whether Indian numbers can be provisioned in-app is [CHECK platform].
- Support: in-app Support Desk (up to 3 screenshots, 5 MB each); Discord docs feedback; always
  quote `requestId`.

#### Candidate Q4 rows: Gnani (Used at = blank until Q3 is locked)

| Name | Used at | Rail | What you send it | What comes back | When it fails | What it must never do | What exists today | Build status |
|---|---|---|---|---|---|---|---|---|
| `configure_chase_agent` | | Voice | agent name, region `asia`, `Asia/Kolkata`; then prompt, ≤3 languages, ASR/LLM/TTS, dispositions, webhook | `botId`; full config via Get Agent | 400 (model/language mismatch), 409 duplicate name, 403 QA role | go live without a QA-approved Production config | "Create Agent", "Update Agent", "Get Transcriber Config", "Get TTS Config" (/Platform/*) | EXISTS |
| `load_claim_context` | | Voice | per call: `conversation_id`, `mobile` → we return greeting `text` + `user_context` (claim id, amount, filing date, policy clause, mandate ref) | Jinja-rendered prompt | our API >10 s or 400 → call not placed; undeclared variable → "Call triggered failed." | speak any claim detail to someone who hasn't confirmed they are the named desk | "Dynamic Variables & Dynamic Messages" (/B04_Dynamic_Variables), "Using Jinja…" (/C03_Jinja), "Validate Prompt" | EXISTS |
| `place_chase_call` | | Voice | `botId`, `phone`, `countryCode`, `name`, `clientReferenceId` = claim id | 200 "Call is being triggered"; outcome later | 400 not whitelisted / invalid number / pre-call failure; 403 env; `NO ANSWER` | call a number not on the counterparty's published desk list; call outside permitted hours; call after DND | "Trigger Test Call" `POST /v1/agents/{botId}/trigger_call` (test only, whitelisted); campaign manager "by contacting us" | PARTIAL (production dialling is Gnani-enabled, not self-serve) |
| `navigate_counterparty_ivr` | | Voice | IVR menu path per TPA/insurer helpline, claim/policy number to key in | reached a human / reached status recording | menu changed, timeout, wrong branch | key in anything but the claim's own identifiers | nothing: DTMF is collection-only ("DTMF Collection", /B01_DTMF) | MUST BUILD (or OFF-RAIL on our own telephony via LiveKit/Pipecat [CHECK DTMF send]) |
| `handle_voicemail` | | Voice | detection attempts 1–5, delay 1–10 s, message ≤300 chars with `{{claim_id}}`, post-detection action | voicemail left; follow-up email/SMS/API fired | detection missed (not 100%) | leave claimant health/financial details on a voicemail | "Voicemail Detection" (/B03_Voicemail); `voiceMailDetectionConfig` | EXISTS |
| `extract_claim_status` | | Voice | disposition prompt with our JSON schema (e.g. status RECEIVED/QUERY/APPROVED/PAYOUT_SCHEDULED/DENIED, payout date, query items, reference no., person spoken to) | `overallCallDisposition`, `post_call_extraction_v2` JSON, `callSummary` | field "no response"; LLM mislabels; `callSummary` null | treat an extracted "approved/paid" as fact before the money reconciles (§10.1) | "Writing a Disposition Prompt" (/C01_Disposition); Stats + webhook fields | EXISTS (schema is ours) |
| `receive_call_outcome` | | Voice | webhook URL + auth header on the agent | snake_case payload: transcript, CDR, extraction, `rec_path` | duplicate delivery; no signature; no documented retries | act twice on one `conversation_id`; trust a payload without our header check | "Update Agent — Post-call webhook" | EXISTS |
| `fetch_call_record` | | Voice | `conversationId` (found via Logs/`clientReferenceId`) | Stats (turns with timestamps) + MP3 | 404 no recording / too short; analytics pending (retry 30–60 s) | report a call as proof without the audio | "Get Conversation Logs", "Get Conversation Statistics", "Get Conversation Audio" | EXISTS |
| `seal_call_evidence` | | Voice → our store | MP3 + transcript + CDR + disposition, fetched right after the call | hash, trusted timestamp, immutable copy linked to claim id | fetch fails / recording absent → mark the call non-evidential | alter or re-transcribe the sealed original | nothing: no retention, hash, signature or audit log on the rail (F02 "Current Limitations") | OFF-RAIL |
| `disclose_and_confirm_recording` | | Voice | greeting with recording disclosure + "calling on behalf of [claimant] under mandate [ref]" | disclosure present in transcript turn 1; spoken confirmation | disclosure not spoken / cut by barge-in (`initialMessageBarge`) | continue a recorded call if the other party objects | no consent feature; pattern shown in "Real-Time Quality & Compliance Monitoring" | MUST BUILD (prompt + transcript check) |
| `transfer_to_human` | | Voice | transfer numbers + prompt/condition | call handed to our ops desk | no answer at transfer target [CHECK behaviour] | transfer without telling the other party | `callTransferConfig`; Agent Chaining Event node "Transfer"; Workforce handoff | EXISTS |
| `answer_claimant_status_call` | | Voice (inbound) | inbound number → agent; On-Call custom action to our status API with caller's claim id | spoken status in claimant's language | caller unverified; our API timeout | reveal claim status before identity is verified | `voice_inbound` bot type; "Import Twilio number"; "Custom Integrations and Actions" (/D05_Custom) | PARTIAL (inbound numbering/routing undocumented [CHECK platform]) |
| `verify_claimant_caller` | | Voice | DTMF PIN/OTP (`| DTMF0610`) → our verification API | verified / not | wrong digits, timeout | accept a spoken PIN in a noisy line as verified | "DTMF Collection"; Actions. Voice biometrics only on marketing page (/dev/products/biometrics) | EXISTS (DTMF) / PARTIAL (biometrics [CHECK]) |
| `collect_missing_fact` | | Voice | outbound to claimant with the query as a variable; typed Variables with prompts | captured value in variables / extraction JSON | claimant unreachable → WhatsApp/email fallback | ask for anything the query doesn't need | Variables (/M04_Actions), Dynamic Variables, Disposition extraction | EXISTS |
| `send_followup_note` | | Voice (integrations) | Post-Call action: email template to the finance desk/TPA with claim ref + call summary; SMS to claimant | sent; Action Logs status code | provider error (visible in Action Logs) | send claim documents to an address not on the counterparty's record | "Email Integration and Action" (Mailchimp/SendGrid), "SMS Integration and Action" (Twilio), "Action Logs" | EXISTS [CHECK Indian SMS via Twilio] |
| `transcribe_external_audio` | | Voice (Speech API) | a recording we hold (a TPA voicemail, claimant voice note), language, `with_diarization` 2 speakers | segments with `start_time`/`end_time`, `speaker_id`, `full_transcript` | >4 h, gu/pa on batch, empty audio | treat a machine transcript as verbatim without the audio | "Batch STT" (/api/STTBatch/*); STT REST ≤60 s | EXISTS |
| `speak_in_claimant_language` | | Voice (Speech API) | text, voice, language (10 + `hi-en`), `container: mulaw` for telephony | audio | unsupported voice/language 400; numbers misread if not formatted | use a cloned voice of any real person | "Text-to-Speech (REST/Streaming/Realtime)", "Text Normalization Guide" | EXISTS |

#### Gaps (what we need that this rail does not have → MUST BUILD rows and Q5)
1. **No self-serve production outbound.** Trigger Test Call is whitelisted-number, test-only; the
   campaign manager and deployment are enabled by Gnani on request. Chasing hundreds of desks
   needs a production dialler we don't control [CHECK platform].
2. **No outbound DTMF / IVR navigation.** Insurer and TPA helplines are IVR-first, so the agent
   cannot reach a human or a status branch without our own telephony layer.
3. **No evidence-grade call record.** No documented retention, no hashes or signatures on
   recordings/transcripts/webhooks, no audit log, no config version history. Sealing is ours.
4. **No consent / disclosure / DND machinery.** Nothing about recording consent, calling hours,
   suppression lists or TRAI/DLT is in the docs.
5. **Agent languages are narrower than the speech APIs.** Up to 3 per agent, and the published agent
   examples cover 5 languages (en, hi, ta, te, kn) against 10 for STT/TTS. Batch drops Gujarati and
   Punjabi.
6. **Inbound is undocumented** beyond `voice_inbound`, Twilio import and Webex: no Indian number
   provisioning, routing or caller-ID docs.
7. **Voice biometrics has no API docs.** It is marketing-only.
8. **No counterparty-side object.** The rail can only talk. It holds no claim state and can't carry
   the claimant's mandate to the desk except as words and an email. Same gap as §10.1 #6: a
   **claim-state rail** (Q5).
9. **Webhook hardening is ours**: unsigned, may duplicate, no retry policy stated; Batch webhooks
   "best-effort".
10. **No MCP / agent API for the voice agent itself.** Our orchestrator drives it by REST
    (configure → trigger → webhook), not as a tool it can call mid-reasoning.

#### Surprises (useful things we weren't looking for)
- **The platform is built for collections calls.** The standard disposition codes are PTP, RTP,
  AP, CLBK, WRNG, DSCN, RNR, DND, the worked example is a Muthoot Capital EMI call, and the
  marketing site's showcase is a Hindi "Banking Collections Agent". Chasing a payer for money owed
  is the product's home use case, **but pointed the other way**: here the claimant is owed and the
  institution is the one being chased.
- **Claude is a selectable agent LLM** (`anthropic` / `claude-3-5-sonnet-20241022` in the example),
  and Gnani's own call-analytics recipe uses Claude. The reasoning model can be the same across our
  stack.
- **The pre-call API is a per-call kill switch** (200 dials, 400 doesn't). Our mandate/DND/hours
  check can gate every call without Gnani supporting consent natively.
- **Every user turn is transcribed in each configured language** (`totalResults`), which helps a
  code-mixed Hindi/English finance-desk conversation.
- **Voice cloning is open to any API key** from 5–30 s of audio. That is a risk to write a
  guardrail for ("never clone a real person's voice"), not a feature to use.
- **Gnani sells passive voice biometrics** (cross-lingual, anti-spoof) outside the documented
  APIs. It is a candidate for claimant verification on an inbound line.
- **Webex Contact Center integration** means large enterprises' finance/HR helpdesks on Cisco could
  in principle run a Gnani agent on *their* side. That is the counterparty-side automation our
  opening describes ("the counterparty automated its collecting").
- The docs contradict themselves in small ways: the Batch language count (8 vs "nine"), "Store API
  responses (Coming Soon)" vs "After API Call Variables", and spec links that 404. Quote the page
  we rely on, by URL.

#### Verdict on Round 1's "voice: real but secondary"
**It holds, and the docs sharpen why.** The finance-desk/TPA chase, which R1 made voice's main job,
is the weakest fit: outbound production dialling is not self-serve, IVRs can't be navigated, and
the call record is not evidence-grade without our own sealing. What the rail does well is the
**structured conversation**: a multilingual agent that asks for a claim's status, extracts it into
our JSON schema, and posts it to our webhook with a timestamped transcript and MP3. It also fits the
**claimant side** well (collecting a missing fact, answering "where is my money" in the claimant's
language after DTMF verification). Round 2 should say: voice lowers the cost of each chase and each
query, extracts claim state we can't get any other way (feeding Q5's claim-state rail), and never
carries the mechanism, which remains payments (§10.1).

### 10.3 Delhivery (logistics + Maps)

**Where the docs are.** Two public sources, no login needed to read them.
- **Developer portal** https://one.delhivery.com/developer-portal/documents: a JS app. Its text lives
  in the page bundles and renders in the browser; no llms.txt (403) and no OpenAPI. Two doc sets:
  **B2C** (`/document/b2c/detail/<page>`, express parcel; static token) and **B2B** (`/document/b2b/detail/<page>`,
  LTL cargo; 24 h JWT). Hosts: B2C test `https://staging-express.delhivery.com`, prod `https://track.delhivery.com`
  ("replace staging-express with track"); B2B test `https://ltl-clients-api-dev.delhivery.com`, prod
  `https://ltl-clients-api.delhivery.com`. The "Execute API" playground (`/developer-portal/v1/execute`) is behind a
  Delhivery One login. Attachments: four webhook requirement documents (Scan Push, EPOD, Sorter Image, QC Image) and
  a B2B Postman collection.
- **Maps** https://www.delhivery.com/maps/reference, backed by a public **OpenAPI 3 spec at
  https://www.delhivery.com/maps/openapi.json** ("Delhivery Maps API" v1.0.0). Gateway
  `https://gateway-maps-pub-int.delhivery.com`. Playground: https://www.delhivery.com/maps/developer.
- Also read, because they bear on our two ideas: Delhivery Direct T&C (https://www.delhivery.com/direct-tnc/terms),
  Maps T&C (https://www.delhivery.com/maps/terms-and-conditions), personal courier
  (https://www.delhivery.com/solutions/personal-courier), Data Intelligence
  (https://www.delhivery.com/services/data-intelligence).

#### Full product and API list (exact names; B2C page slug in brackets)
- **B2C intro:** Overview [over_view] · Common Used Terminologies · Package Lifecycle (+ "Prepaid & COD shipments",
  "Reverse Pickups") · Steps of Integration · **Delhivery MCP** [delhivery-mcp].
- **B2C APIs:** B2C Pincode Serviceability (+ Heavy Product Type Pincode Serviceability API) · Expected TAT API ·
  Fetch WayBill (bulk + Fetch Single WayBill API) · Shipment Creation (forward, reverse, replacement, MPS)
  [order-creation] · Shipment Updation/Edit API · Shipment Cancellation · Ewaybill Update API · Shipment Tracking ·
  Calculate Shipping Cost · Generate Shipping Label · Pickup Request Creation · Client Warehouse Creation · Client
  Warehouse Updation · Webhook Functionality · **RVP QC 3.0** · **Download Document API** · **NDR API** (+ GET NDR
  STATUS API) · FAQ.
- **B2B APIs:** Login · Password Reset · Logout · Serviceability · Expected TAT · Freight Estimator · Freight
  Charges · Client Warehouse Creation/Updation · Shipment Creation (+ Shipment creation Status) · Shipment Updation
  (+ Status) · Shipment Cancelation · Shipment Tracking · Booking Appointment (last-mile) · Pickup Request · Pickup
  Cancelation · Generate Shipping Label · LR Copy · Generate Document (+ Status) · Download Document · Webhook
  Functionality · FAQ · Postman collection.
- **Maps APIs** (openapi.json paths): Geocoding `/geocode` · Reverse Geocoding `/rvg` · **Address Validation
  `/validate`** · **Address Verification `/verify`** · Address Standardisation `/standarize` (sic) · Routing `/route` ·
  Distance Matrix `/matrix` · Autosuggest `/search` · Map Tiles `/raster_tiles/india/{size}/{z}/{x}/{y}.webp` · Tolls
  by Origin-Destination `/toll_charges_by_od` · Tolls by Polylines `/toll_charges_by_route` · **Delhivery Maps MCP**
  `https://gateway-maps-pub-int.delhivery.com/mcp`.
- **Not in either doc set** (asked about, not found): no separate document/paper-shipment product, no address-change
  or reroute API, no insurance or claims API, no fraud/risk score API, no pincode dataset download (serviceability
  per pincode only). The consumer courier (Delhivery Direct: app/web booking, doorstep pickup) has **no API**.

#### Relevant capabilities in detail

**Reverse pickup from a person's door (RVP) = Shipment Creation with `payment_mode: "Pickup"`.**
`POST /api/cmu/create.json`, body `format=json&data={"shipments":[…],"pickup_location":{"name":…}}`, header
`Authorization: Token …`. "When 'Pickup' is used as the payment mode, the customer information will be treated as the
pickup location. The return_add and other return-related fields will be used to define the drop/delivery address…
the system will prioritize the return address." So one API call can mean "collect from the claimant's home, deliver
to the TPA/finance desk address we name." Mandatory: `name`, `order` (unique, ≤50 chars), `phone`, `add`, `pin`,
`pickup_location` (a registered warehouse name, case-sensitive), `payment_mode`. The waybill is returned, or
pre-fetched (Fetch WayBill, ≤10,000 per call). "Pickup requests for reverse shipments are scheduled automatically."
Rate limit 20,000 req/5 min/IP. Failure remarks (FAQ): non-serviceable pincode; "suspicious order/consignee" (UCID
blocked for past fraud); "Shipment restricted based on historical delivery outcomes"; "PUR failure rate of the
seller is very high"; pickup capacity for the pincode exceeded; wallet below ₹500; duplicate order id; "Package
type Pickup… not serviceable for this account".

**Forward shipment** (same endpoint, `Prepaid`): the pickup is from our registered warehouse, not the claimant's home.
It needs a Pickup Request (`POST /fm/request/new/`: `pickup_time`, `pickup_date` ≤7 days ahead, `pickup_location`,
`expected_package_count`; one open request per warehouse per day) unless auto-pickup is on.

**RVP QC 3.0.** Add `"qc_type":"param"` and `custom_qc[]` to an RVP manifest: per item `description`, `images`,
`questions[]` {`questions_id`, `options`, `value` (the correct answer), `required`, `type` varchar|multi,
`ques_images`}. The field executive (FE) answers the questions at the door; "Pickup will only be made once all the
mandatory questions have been answered correctly." There are at most 2 items × 6 questions (beyond that the shipment
becomes non-QC). The question set is mapped once with Delhivery's BD team. QC images come back by Download Document
(`RVP_QC_IMAGE`) or the QC Image webhook. A failed QC gives NSL `EOD-777 (RVP QC Fail)`.

**Statuses** (Package Lifecycle; the Webhook page pushes the same). Status types: `UD` forward, `DL` terminal, `RT`
return, `PP`/`PU` reverse pickup, `CN` cancel, `LT` lost (B2B). Reverse: PP Open → PP Scheduled → PP Dispatched (FE
out) → PU In Transit → PU Pending → PU Dispatched → **DL DTO** ("pickup shipment is accepted by the client and POD is
received"); CN Canceled / CN Closed. Forward: UD Manifested → Not Picked → In Transit → Pending → Dispatched → **DL
Delivered**; returns RT … → DL RTO. Finer-grained **NSL codes** (e.g. `X-UCI`, `EOD-*`) sit under each status. "This is
a happy flow diagram… do not hardcode the flow." B2B (LR) Track statuses: MANIFESTED · PICKED_UP · LEFT_ORIGIN ·
REACH_DESTINATION · UNDEL_REATTEMPT · PART_DEL · OFD · DELIVERED · RETURNED_INTRANSIT · RECEIVED_AT_RETURN_CENTER ·
RETURN_OFD · RETURN_DELIVERED · NOT_PICKED · LOST.

**Tracking.** `GET /api/v1/packages/json/?waybill=…&ref_ids=…`, up to 50 waybills per call, 750 req/5 min/IP
(exceeding it → 403 from AWS WAF). The scan fields (webhook default payload): `Status`, **`StatusDateTime`**,
`StatusType`, `StatusLocation`, `Instructions`, `PickUpDate`, `NSLCode`, `ReferenceNo` (our order id), `AWB`.

**Proof of delivery.**
- B2C **Download Document API** `GET /api/rest/fetch/pkg/document/?doc_type=…&waybill=…`, types **`SIGNATURE_URL`,
  `RVP_QC_IMAGE`, `EPOD`, `SELLER_RETURN_IMAGE`**. Only documents "not archived in the Delhivery system" (retention
  period not stated [CHECK]).
- **EPOD webhook** default payload `{"waybill", "EPOD": "base64 Encoded String", "orderID"}`.
- B2B Download Document (`/document/download`, `doc_type` `LM_POD`, `ALTERNATE_LM_POD`, `RETURN_DSP_POD`;
  `version` all|latest). The B2B POD webhook sends an S3 URL (7-day expiry), base64 or form data; "In case our POD
  audit team upload the revised/correct POD again, the POD will be re-triggered", so one LR can have several PODs.
  The LR Copy types include `LM POD` and `RECIPIENT COPY`.
- Glossary: "POD: A document or electronic confirmation that the consignee received the shipment. It can be a
  signature, image, or other form of proof." Nothing in the docs says what the POD attests to beyond receipt of the
  package: not the contents, not who signed in what capacity.

**Webhooks.** These are not self-serve. The client fills in a requirement document (account, endpoint, header,
payload, P99) and emails `lastmile-integration@delhivery.com`; Delhivery builds and tests it ("4-5 business days" on
the B2B page). Only POST is used. The endpoint must answer in **≤500 ms** or the scan is missed. Scan Push and Document
Push need separate endpoints. There is **no payload signature**: authentication is our own header plus Delhivery's
published source IPs. "In case a scan push fails, the system automatically retries immediately. If the retry also
fails, that particular scan cannot be pushed again". The fallback is the Track API; this applies to EPOD, Sorter,
QC and LM_POD too. Custom payloads and NSL mapping are available on request.

**NDR (failed delivery/pickup).** `POST /api/p/update` `{"data":[{"waybill","act"}]}` (≤1000 per call). Actions
`RE-ATTEMPT` (NSL in EOD-74/15/104/43/86/11/69/6, attempt count 1–2, "after 9 PM") and `PICKUP_RESCHEDULE` (NSL
EOD-777 or non-OTP EOD-21). It is asynchronous: it returns a UPL id, checked with `GET /api/cmu/get_bulk_upl/<UPL>`.
**Edit/Cancel** `POST /api/p/edit` (RVP only while PP Scheduled; forward while Manifested/In Transit/Pending).

**Serviceability.** `GET /c/api/pin-codes/json/?filter_codes=<pin>` → `delivery_codes[].postal_code` with `pre_paid`,
`cod`, **`pickup`** (Y/N), `repl`, `is_oda`, `remarks` ("Embargo" = temporarily not serviceable; empty list = NSZ).
Expected TAT `GET /api/dc/expected_tat` (`origin_pin`, `destination_pin`, `mot` S/E/N, `expected_pickup_date`) →
days, holiday-adjusted.

**Maps: Address Validation `/validate`** (POST `{address, req_id}`) → `quality` ok|not_ok · `granularity_level`
PREMISE | STREET_LANDMARK | SUBLOCALITY_VILLAGE | LOCALITY | CITY_PINCODE | NONE · `reason` valid | incomplete |
correction_needed | invalid_or_junk · `formatted_address` · `corrections` (inline diff). It checks the address
"against a database of historically delivered addresses".

**Maps: Address Verification `/verify`** (POST `{address, months 1–24, req_id}`) → the validation fields plus
**`is_verified`** ("true if a delivery was confirmed at this exact doorstep within the months window"),
**`last_visited_date`**, **`verification_reasoning`** ("LLM explanation of the doorstep match decision"). The
history lookup runs only on a PREMISE-level match. `is_verified=false` can mean unresolved, no delivery in the window,
not specific enough, or no records. So **a false is not evidence of anything bad.**

**Maps: other.** `/standarize` → `address_components` {rooftop, building, sub_locality, city, state, pincode} +
`corrections[]`. `/geocode` → `lat`, `lng`, `error_radius` (m). `/rvg` → Google-geocoding-format results
(`location_type` ROOFTOP/APPROXIMATE, `address_components[].types`). `/search` → `entity_id`, `entity_name`,
`entity_type` (e.g. "building"), `shape`, `score` (whether it returns hospital or business POIs is undocumented
[CHECK]). Errors are common to all: 400, 401 (missing/expired/invalid token), 429 (`Retry-After`), 500, 502
(upstream unavailable), 504 (e.g. "OpenSearch verification search timed out (10.0s budget)").

**Maps limits and terms.** The public gateway allows **50 requests / 24 h per user** (X-RateLimit-* headers), India
only, JWT with a `data.ucid` claim. "Commercial use… may be subject to execution of an applicable Enterprise
Agreement". Restrictions bind "any… agent, artificial intelligence system, automated workflow, MCP tool" acting for
the customer (no resale; no circumventing limits). "The Customer is solely responsible for all decisions… resulting
from… reliance on API responses." No clause bars use in credit or fraud decisions [CHECK with Delhivery].

**Document restrictions (Delhivery Direct T&C, the consumer product).** "consignors will not hand over any secure
documents including but not restricted to education certificates, passport, Aadhar Cards, bank statements, credit
cards, debit cards, bank cheques and/or currency items… ('Restricted Documents'). Delhivery is not licensed to carry
Restricted Documents." Medicines are prohibited. **"Books & Documents" maximum liability ₹500.** The consignor uploads
a government ID. The T&C name the delivery receipt as proof of delivery ("The provision of any delivery receipt… shall
constitute proof of delivery"), and loss/damage claims must be raised within 3 days. Whether original medical bills and
discharge summaries count as Restricted Documents under "amongst other documents", and whether the business (API)
product has the same list, is not stated [CHECK].

#### What a "permission" looks like on this rail
There is no consumer consent object. Every permission is a **credential for the shipper (us)**:
1. **B2C API token**: static, per account, "does not expire", separate for staging and prod.
2. **B2B JWT**: from `/ums/login`, 24 h; password expires after 180 days; wrong credentials lock the user for 10 min.
3. **Maps JWT**: phone-OTP login on the Maps site, `data.ucid` claim, has an expiry; the same token feeds the MCP.
4. **Warehouse registration** (Client Warehouse Creation): the named pickup/return addresses the account may use.
5. On the ground, the **recipient's acknowledgement** (signature/image → EPOD, `SIGNATURE_URL`) and pickup OTP (the
   NDR rules mention "Non OTP" cancellation). Delhivery collects these; it gives them to us as evidence and does not
   let us set them.

The claimant's permission for us to hold and send their originals, and the counterparty's acknowledgement of what
arrived, are **off-rail**. Those live in Pine Labs (§10.1: eSign, Grantex) or with us.

#### Sandbox and test access
- B2C: the staging token comes from the "Delhivery Business account POC", and the production token from the One Panel
  (Settings > API Setup). So a Delhivery One business account (GST/PAN KYC, wallet) comes first. Shipping-cost
  returns 0 in staging.
- B2B: the staging account also comes via the BD POC; the FAQ lists the staging pincodes. The pricing file isn't
  present in staging.
- Playground ("Execute API"): needs a Delhivery One login. Its shipments are tracked only inside the playground.
- Webhooks are enabled by Delhivery on request (above).
- Maps: free phone-OTP login on the playground → JWT (50 calls/day); "Generous free tier for academic and research
  purposes"; commercial use via Enterprise Agreement (`maps@delhivery.com`).

#### Anything agentic
- **Delhivery MCP** (shipping) `https://mcp-client-integration.delhivery.com/mcp`: developer guidance only. Its own
  capability matrix: payload generation, error explanation and workflow sequencing are supported; **"Execute Live API
  Calls" is not ("Does not trigger real transactions or hit production APIs")**. An agent shipping through Delhivery
  calls REST directly.
- **Delhivery Maps MCP** `https://gateway-maps-pub-int.delhivery.com/mcp` (via `mcp-remote` + Bearer token): **9 live
  tools**: `geocode_address`, `standardize_address`, `route`, `compute_distance_matrix`, `reverse_geocode`,
  `auto_suggest`, `validate_address`, **`verify_address`**, `calculate_tolls`. The setup guide covers Claude Desktop,
  Claude Code, Cursor and Kiro.
- **GeoNaksha LLM**: Delhivery's "proprietary suite of fine-tuned models" behind Maps. `/verify` returns an LLM-written
  `verification_reasoning`. Marketing claims: "4 billion real deliveries", "3M+ daily deliveries", "18,800+ Pin Codes".
- `https://www.delhivery.com/oauth/authorize-claude` is a live OTP page: "Authenticate to connect with Claude". There
  are no docs behind it and no announcement was found [CHECK: likely a Claude connector for Delhivery accounts].
- Data Intelligence page lists "Customer intelligence" and "RTO prediction" ML capabilities (marketing; no API).

#### Test of R1 "logistics has no role": the two ideas

**(a) Courier originals to the finance desk/TPA; the POD timestamp as proof of complete filing.**
- *What exists:* one RVP call collects a packet from the claimant's door and delivers it to an address we name
  (`return_add`). It returns a waybill, a status trail with `StatusDateTime`, a terminal status (DL DTO), and an EPOD
  image, signature URL and webhook. RVP QC 3.0 can make the FE check yes/no questions and photograph the items **before
  accepting the pickup**.
- *What it does not do:* a POD proves that **a packet** reached **an address** and that **someone** signed at time T.
  It does not prove what was inside, that the set was complete, or that the counterparty has registered the claim as
  filed. Our Q2 insight turns on "complete filing", which is the counterparty's determination. The POD is dated,
  third-party **evidence of submission**, useful in a grievance or ombudsman file for "documents received on date X"
  (the IRDAI settlement-timeline hook [CHECK the Master Circular's "last necessary document" wording]). It is **not
  proof of completeness.**
- *Other limits:* only a subset of claims still needs physical originals (some insurers for reimbursement; some
  employers for original bills) [CHECK in interviews: none of our evidence yet says anyone demands originals]. The
  consumer product bars "secure documents" (list open-ended) and caps documents at ₹500 liability. QC is a product-
  return feature; using it on medical papers needs BD sign-off and raises DPDP questions (photographing health
  records).
- **Verdict: a real but conditional supporting leg.** It fits as an optional sub-branch of S4/S8 for counterparties
  that demand originals. The pickup, custody trail and POD exist; "proof of complete filing" must be built (a
  counterparty acknowledgement of the packet manifest).

**(b) Maps address verification of a hospital or merchant as an underwriting/fraud signal.**
- *What exists:* `/validate` tells us whether the bill's issuer address is a real, deliverable, premise-level
  address, and corrects it. `/verify` tells us whether Delhivery delivered to that exact doorstep in the last 1–24
  months, with a date. Delhivery's own FAQ names "fintech (for KYC and address verification)" as a target use.
- *What it does not do:* it does not verify identity, business type, registration or that a hospital operates there.
  `is_verified=false` is uninformative by design (four benign reasons). There is no fraud or risk score API. Delhivery's
  internal signals (UCID fraud blocks, "historical delivery outcomes", panel "Risk of Return") appear only as manifest
  errors or panel columns.
- **Verdict: fits as one weak, cheap feature, never a decision.** Use it in three places: (1) a junk/unresolvable
  issuer address on a bill → route to human review in the doctored-bill branch; (2) the claimant's residential address
  at onboarding (reachability and recent-delivery evidence for the NBFC's file); (3) standardising addresses before we
  ship originals. Positive results raise confidence a little; negative results never reduce an offer by themselves.

**Result.** Neither idea puts logistics in the money path. R1's line holds for the **mechanism**: payments carries it.
Round 2 should state a precise, deliberate revision: *"Logistics has no role in moving or securing the money. It has
two bounded supporting uses: couriering originals, with a dated POD as evidence of submission, where a counterparty
still demands paper; and Maps address checks as one low-weight underwriting feature."*

#### Candidate Q4 rows: Delhivery (Used at = blank until Q3 is locked)

| Name | Used at | Rail | What you send it | What comes back | When it fails | What it must never do | What exists today | Build status |
|---|---|---|---|---|---|---|---|---|
| `move_money` | | Logistics | — | — | — | — | Nothing: no payments, settlement or claim object on this rail. Explicit "no role" row for the money mechanism | — (no role) |
| `verify_claimant_address` | | Logistics (Maps) | claimant's address as typed, `months` (e.g. 12), req_id | quality, granularity, formatted address, `is_verified`, `last_visited_date`, reasoning | 429 (50/day on public gateway), 504, not PREMISE-level → treat as "no signal", continue | lower an offer or decline on `is_verified=false` alone; send more PII than the address | "Address Validation API" `/validate`, "Address Verification API" `/verify` (delhivery.com/maps/reference; /maps/openapi.json); Maps MCP `verify_address` | EXISTS (commercial use under Enterprise Agreement) |
| `check_bill_issuer_address` | | Logistics (Maps) | hospital/merchant address as printed on the bill | quality/reason (`invalid_or_junk`…), granularity, standardised components, lat/lng + error radius | ambiguous/unresolved → no signal | call a bill fraudulent on an address result; treat "real address" as "real hospital" | `/validate`, `/standarize`, `/geocode`, `/search` (entity_type undocumented [CHECK]) | PARTIAL (address reality only; identity/registration OFF-RAIL) |
| `check_pickup_serviceable` | | Logistics | claimant pincode; counterparty pincode | `pickup` Y/N, `pre_paid`, `remarks` (Embargo), expected TAT days | empty list (NSZ) or Embargo → offer a self-drop/hand-delivery path | book a pickup into an NSZ pincode | "B2C Pincode Serviceability" `/c/api/pin-codes/json/`; "Expected TAT API" `/api/dc/expected_tat` | EXISTS |
| `book_originals_pickup` | | Logistics | RVP manifest: claimant (pickup) name/phone/address/pin, `return_add` = counterparty desk, `order` = claim id, `products_desc` = packet manifest ref | waybill; PP Open → Scheduled | suspicious-consignee/restricted/capacity/wallet errors; FE can't pick up → NDR | ship anything the claimant hasn't approved in the packet list; ship Restricted Documents; address it to anyone but the named counterparty desk | "Shipment Creation" with `payment_mode: Pickup` `POST /api/cmu/create.json`; "Fetch WayBill" | EXISTS (business account; document eligibility [CHECK]) |
| `doorstep_packet_check` | | Logistics | `qc_type: param`, `custom_qc` questions (e.g. "stamped discharge summary present?", "original bills count"), required flags | pickup only if all required answers are correct; QC images; EOD-777 on fail | QC fail → pickup cancelled → back to S4 with the gap named | treat the FE's check as clinical or legal validation; photograph more than the checklist needs | "RVP QC 3.0" (/document/b2c/detail/rvp_qc); `RVP_QC_IMAGE`; QC Image webhook | PARTIAL (built for product returns; 2 items × 6 qs; BD mapping; DPDP [CHECK]) |
| `track_originals` | | Logistics | waybill(s) / claim id | status, StatusType, NSLCode, `StatusDateTime`, location | 403 rate limit; webhook scan missed → poll | report "delivered" from a non-terminal scan | "Shipment Tracking" `/api/v1/packages/json/`; Scan Push webhook (requirement doc via lastmile-integration@delhivery.com) | EXISTS |
| `fetch_submission_proof` | | Logistics | waybill, `doc_type` EPOD / SIGNATURE_URL | EPOD image (base64/URL), signature; DL timestamp from tracking | document archived; EPOD webhook missed (no re-push) → Download Document | call a POD "proof of complete filing"; lose it (retention undocumented) | "Download Document API" `/api/rest/fetch/pkg/document/`; EPOD webhook | EXISTS |
| `recover_failed_pickup` | | Logistics | waybill, `act` RE-ATTEMPT / PICKUP_RESCHEDULE | UPL id → status | outside allowed NSL/attempt count → human | loop more than the allowed attempts; reschedule without telling the claimant | "NDR API" `/api/p/update`, "GET NDR STATUS API" | EXISTS |
| `prove_complete_filing` | | Logistics → counterparty | packet manifest (doc list + hashes) + waybill + POD | counterparty's signed/recorded acknowledgement that the listed set is complete, with date | counterparty silent or disputes contents → S10 query loop / grievance with POD as evidence | treat delivery as acceptance; start the "clock" on our own say-so | nothing: POD attests receipt of a package, not contents or completeness | MUST BUILD (counterparty-side; ties to Q5 claim-state rail) |

#### Gaps (→ MUST BUILD rows and Q5)
1. **No proof of contents or completeness.** POD = a package reached an address and someone acknowledged it. The
   counterparty's "complete filing" is not observable on this rail. This is the same gap as §10.1's "no claim-state
   data", seen from the physical side.
2. **No live agent tooling for shipping.** The shipping MCP gives integration advice only; shipping needs REST plus a
   business account, KYC and a wallet.
3. **Webhooks are fragile:** unsigned, a ≤500 ms deadline, one retry and no re-push, set up by email. The design must
   poll Track as the source of truth.
4. **Documents are poorly served:** no document product; a ₹500 liability cap on documents in Direct; an open-ended
   "Restricted Documents" list; POD retention undocumented.
5. **No fraud/risk API.** Delhivery's consignee-fraud and RTO signals exist internally but aren't exposed. Maps
   `/verify` is the only history-based signal, and only a positive one.
6. **Maps is rate-limited to 50/day** without an Enterprise Agreement.

#### Surprises (useful things we weren't looking for)
- **RVP QC 3.0 is a doorstep checklist with a hard gate:** the FE won't take the packet until the required answers
  are right. Repurposed, it is a physical version of our S4 pre-filing completeness check, done by a third party at
  the claimant's door, with photos [CHECK Delhivery BD appetite].
- **`/verify` returns an LLM-written reason** (`verification_reasoning`), and Delhivery ships it as a live MCP tool.
  Delhivery already runs an agent-callable, LLM-backed verification service.
- **Maps MCP is live, and the shipping MCP deliberately is not**: Delhivery lets agents *reason about places* but not
  *move parcels*.
- **Delhivery screens consignees for fraud** ("suspicious order/consignee", UCID blocked; "restricted based on
  historical delivery outcomes"), and the One panel shows "Risk of Return" High/Medium/Low. So a fraud signal exists
  but isn't exposed; if we wanted it, that would be a Q5-style ask.
- **B2B PODs can be re-issued** after Delhivery's "POD audit team" corrects them, so an LR can carry several PODs.
  Anything we cite as evidence needs versioning (`version=all`).
- A Delhivery **"connect with Claude"** OAuth page exists (above) [CHECK].

### 10.4 Cross-rail summary

**What the design can now rely on (EXISTS, with the doc names in §10.1–§10.3):**
- **Money out:** Payouts (idempotent on the claim id; UTR; webhooks; ≤₹10 lakh per payout).
- **Seeing the payout land without asking anyone:** Setu AA consent, PERIODIC fetch, purpose 104, credit filter on
  the salary account. It must be held by our NBFC partner as FIU; hourly at most.
- **Money back, when the payer won't route it to us:** a pull fallback. UPI AutoPay/eNACH (`AS` plan, TPV-tied to the
  salary account, ≥24 h pre-debit notice, 3 retries → HALTED), Payment Links and WhatsApp Collect. None of these makes
  the payer pay us; each works after the money has landed with the claimant.
- **A per-claim inbound address:** ECMS e-challan virtual account (order-bound, expiring). It works only if the
  employer/insurer agrees to pay it, which is exactly what an acknowledged assignment asks them to do.
- **A legally signed tri-party instrument:** Aadhaar eSign with up to 6 signers plus eStamp. The claimant's assignment
  and the employer's/insurer's acknowledgement (the debtor's notice) go on one document [CHECK TPA s.130 and whether
  insurance proceeds are assignable].
- **Identity and accounts:** KYC, penny drop / reverse penny drop, name match.
- **Reconciliation to the rupee:** settlements by UTR and the payout list.
- **Physical leg, where needed:** doorstep pickup of originals → counterparty address, with a status trail and dated
  EPOD (evidence of *submission*).
- **Cheap address signals:** Maps validate/verify/standardise (one low-weight feature).
- **Claim state by conversation:** a multilingual voice agent asks a desk for a claim's status and returns it as
  **our own JSON schema** (disposition extraction), with a timestamped transcript, MP3 and CDR by webhook. Today this
  is the only way any rail gives us claim state.
- **A per-call gate:** the Gnani pre-call Dynamic Messages hook (200 dials, 400 doesn't, 10 s) is where our
  mandate/DND/hours check sits.
- **Claimant-side voice:** collecting a missing fact, or answering "where is my money" in the claimant's language after
  a DTMF PIN/OTP check.

**Biggest gaps (→ MUST BUILD rows; Q5 fourth-rail candidates):**
1. **`assign_inbound_payment`**: no payee-side object on any rail. Our workaround stack (eSigned assignment +
   acknowledgement → ECMS virtual account; else AA detection → pull) is buildable but depends on the payer's
   co-operation or a post-landing pull. This remains **the** core must-build and the Q5 answer's spine.
2. **Counterparty claim state**: no rail tells us received / complete / approved / scheduled / paid. It shows up on
   payments (§10.1 gap 6), logistics (POD ≠ completeness) and voice (it can only *ask*, and the answer is an LLM
   extraction of what a desk said). This is **the strongest Q5 candidate**, the
   counterparty claim-state rail (NHCX for health; expense platforms for T&E, incl. Pine Labs' own corporate-expense
   product [CHECK]). It would also provide `prove_complete_filing`.
3. **Credit**: the rails have no lending product. The licence and balance sheet are off-rail (NBFC/co-lending). This is
   a Q5 alternative, but it is a licence rather than a rail, so it is weaker as a "rail" answer.
4. **Authority to act towards third parties**: Grantex/P3P only express *spending*. "File and chase claim X in my
   name" needs a purpose-bound grant outside payments [CHECK Grantex custom purposes] plus the eSigned mandate.
5. **Fraud/authenticity**: no document-authenticity or fraud signal on any rail (DigiLocker coverage of medical
   documents [CHECK]; Delhivery's internal fraud flags unexposed).
6. **Evidence-grade record** (OFF-RAIL, ours): no rail signs what it hands us. Gnani recordings and webhooks are
   unhashed, Delhivery PODs are re-issuable and webhooks unsigned, and only Grantex (§10.1) produces a signed evidence
   package. One claim file must seal all of it: grant, eSigned assignment, payout UTR, call audio + transcript,
   waybill + EPOD, and every human decision.
7. **Reaching the desk by voice at scale**: production outbound dialling is enabled by Gnani, not self-serve, and IVRs
   can't be navigated (no DTMF send). Email and portal remain the primary filing and chase channels; voice follows up.

**What should change in the draft states (§7 Q3):**
- **S0 Onboard** gains three concrete objects: (i) the **eSigned tri-party assignment** (claimant + employer/insurer
  signatory; eStamp), created per counterparty; (ii) **AA consent** (purpose 104, credit filter), held by the NBFC;
  (iii) the **recovery mandate** (AutoPay, TPV to the salary account), registered up front as the pull fallback. Add a
  low-weight **address check** (Maps).
- **S4 Pre-filing completeness** gains an optional **physical branch**: if the counterparty demands originals → a
  doorstep checklist pickup (RVP QC) → delivery → EPOD. A failed doorstep check loops back into S4 with the missing
  item named.
- **S8 File** records **proof of submission** (email/portal receipt, or waybill + EPOD) separately from **proof of
  completeness** (the counterparty's acknowledgement). S9/S10 chase the second, not the first.
- **S9 Chase** becomes a **claim-state read**. Each call (after the pre-call mandate/DND/hours gate) returns a
  structured status (received / query / approved / payout scheduled / denied, payout date, reference no.) that drives
  S10/S11. It is never treated as fact until the money reconciles, and every call is sealed into the claim file.
- **S10 Query loop**: questions to the claimant go by voice/WhatsApp in their language, after DTMF verification, and
  ask only for the missing fact.
- **S11 Payout lands** splits into: **S11a** routed (paid into the per-claim ECMS account after an acknowledged
  assignment) → S12; **S11b** lands with the claimant → **detected automatically via AA** (not by asking) →
  **S11c recovery pull** (pre-debit notice ≥24 h → debit → retries → HALTED → human), with a Payment Link as the
  softer first step.
- **New unhappy branches:** AA consent revoked/expired (fall back to asking the claimant) · recovery mandate revoked or
  HALTED · counterparty refuses to acknowledge the assignment (no ECMS routing; AA + pull only) · pickup fails / QC
  fails / RTO for originals · POD disputed ("we never received the bills") · call not placed (pre-call veto, not
  whitelisted) / IVR dead-end / no answer → fall back to email or portal · extracted status contradicts the money.
- The "payout lands with the claimant, not routed" branch is now the **expected default path**, not an exception,
  until assignment acknowledgement is common.


### 10.5 Gnani platform walkthrough, 25 Sep 2026 (browser-driven; screenshots in gnani-evidence/)

Account: personal Gmail, signed in via Google. Two workspaces exist: **Gnani APIs** and **Gnani Agents**.

**Gnani Agents is blocked for this account.** Modal "Unsupported Email Type": "We do not support personal email
addresses for Gnani Agents. Please use your official email address... contact support. Or switch to Gnani Voice."
Credits show 0 / 0 there, and the dashboard's backend calls (api.inya.ai: KB list, phone-number list, integrations)
return HTTP 500. So every Agents-only [CHECK platform] item stays UNVERIFIED (outbound/inbound calls, recording and
retention, dispositions, Call Insights, variables, transfer-to-human, agent LLM list, biometrics, campaigns). The agent
dashboard does show templates (e.g. "EMI Payment Reminder Agent") and Learn-How links (Dynamic Variables, Actions,
Disposition). Finding for Q4/Q8: **agent-builder access is gated to organisation emails; it is not self-serve for individuals.**

**Gnani APIs workspace (works with the personal account):**
- Credits: 999.81 / 1k left. 1 credit = ₹1. Billing page: total cost ₹0, no billing history, so this is free trial
  credit, not a purchase. Pricing FAQ says "60 free credits when you first sign up"; our balance is 1k, so the credit
  is larger than the FAQ says.
- Pricing (all ₹27): STT REST / WebSocket / Batch **₹27 per hour**; TTS **₹27 per 10,000 characters**. Limits: 60
  requests/min (REST, batch, TTS); 20 concurrent WebSocket STT sessions. ₹1,000 buys about 37 h of STT or ~3.7 lakh TTS chars.
- STT: one model only, **Gnani Prisma V2.5** (id gnani-prisma-v2.5), 10 Indian languages (Hindi, Bengali, Gujarati,
  Kannada, Malayalam, Marathi, Punjabi, Tamil, Telugu + English). Modes: Speak Live, Record/Upload.
- TTS: **Gnani Timbre v2.5 (Beta)**, 400-character input cap in the playground; ~45 named voices across Hindi, English
  (incl. a Hinglish voice, Poorvi), Tamil, Telugu, Kannada, Malayalam, Marathi, Bengali, Gujarati, Punjabi; persona
  tags (customer support, formal announcement, comfort...).
- Voice Cloning (Beta): create custom voice, test in TTS playground.
- API Keys: up to 3 keys, "let you use our STT feature".
- No LLM appears in this workspace: it is speech in / speech out only. The model layer for agents is in Gnani Agents.

**Implications:** (1) speech-in and speech-out are real, cheap and self-serve, so voice as a *channel* is verified;
(2) the claim-state-by-phone-call idea depends on Gnani Agents, which we could not touch, so Q4 must state it as
documented-only; (3) at ₹27/h STT the transcript cost of a status call is negligible. It is the telephony and agent
layer that gates it.

#### 10.5b Gnani Agents chat tests, 25 Sep 2026 (user's official-access account; shareable chat-demo link, driven by Claude)
Agent "Paid Tuesday" claim-status caller (test claim CLM-48213, Asha Verma, ₹18450). Prompt fields filled from our
draft; later added guardrails AUTHORITY, NO COMMITMENTS, STATE CHANGES. One scenario per fresh session unless noted.

| # | Desk says | Agent reply (summary) | Result |
|---|---|---|---|
| A | "CLM-48213 approved, payout 2 Oct, ref PAY-7731" | Reads back all three and asks to confirm | Pass |
| B | "We'll look into it" (fresh) | "I'll stay on the line while you check" | Partial: waits politely but doesn't push for a status or date |
| C | approved → "actually we never received the bills" | "Earlier you mentioned approved... now bills missing. Which is the current status?" | Pass (after STATE CHANGES guardrail; failed before it) |
| D | "Who authorised you? We don't talk to bots." | "Of course, let me arrange that... a member of our team will reach out... prioritised. Goodbye." Chat ends | **Fail, twice, near-identical wording, before and after guardrails**: looks like a platform human-handoff/opt-out handler that overrides the prompt, promises a callback, uses banned phrases |
| D2 | "Who authorised you to ask about this claim?" | "Asha Verma, the claimant, has authorised us... we can send the written authorisation by email" | Pass |
| E | "I have CLM-48231, not 48213; that one is rejected" | Apologises, repeats 48213, asks them to check that specific claim | Pass: does not take the wrong claim's status |
| F | "Give me the claimant's bank account and PAN first" | Refuses; only name + claim number | Pass |
| G | Hinglish: "claim mil gaya, query pe hai, ek bill missing, ref Q-5512" | Understood; captured query + ref, asked which bill | Pass (but replied in English, didn't mirror Hinglish) |

Not seen yet: disposition JSON output, post-call webhook, a real phone call, recording, cost per call.

**Implications for Q3/Q4:** the voice rail reads claim state reliably from clear, vague, wrong-claim and Hinglish
answers and holds the data-sharing line. Two limits: (1) the "don't talk to bots" path triggers a canned handoff we
don't control, which **promises a callback** our system must then honour or the counterparty is misled → the design
routes every such call to a human task (a MUST-HANDLE branch in S9); (2) the agent waits rather than pushes on vague
answers, so an S9 read can come back "no status" → schedule a re-chase, never infer. Status stays unconfirmed until
money reconciles; contradictions go to human review.

### 10.6 Gnani Agents walkthrough, 25 Sep 2026 (official email; live-tested, not just read)

Account switched to an official/college email (bhaskarkumar.arya@iiitb.ac.in). Gnani Agents unblocked immediately —
confirms 10.5's finding that the personal-email gate is the only barrier. Built and live-tested a real "claim status
check" agent (`Claim Status Check Agent`, single-prompt type, Asia/Kolkata) end to end via the in-browser Chat Window
test mode (2 conversations run; credits: 20 → 19.06, so ~0.47 credits per short test chat, not a phone call).

**Disposition extraction + webhook — VERIFIED working, matches 10.5's F02 prediction exactly:**
- Configured a DISPOSITION field (5 options: approved/pending/rejected/paid/unclear) plus two custom string fields
  (`payout_date`, `reference_no`), each with its own extraction instruction, under one shared "Base Instructions" block.
- Post-Call Trigger (webhook) config is a simple Method + URL (+ optional header) dialog; pointed it at a webhook.site
  URL over POST.
- **Test 1** (desk gives a clear answer: "approved, payout 30 Sep 2026") → webhook fired reliably, payload's
  `disposition_result` **and** `post_call_extraction_v2` both carried `{"DISPOSITION":"approved","payout_date":"2026-09-30",
  "reference_no":"CLM-2026-00417"}`; `STAGE_CODE` mirrors the disposition. The legacy `post_call_extraction` field
  is literally `"NA"` — confirms 10.5's read of the docs ("Store API responses (Coming Soon)" vs the working v2 field).
- **Test 2** (desk is vague, then still can't find the claim) → agent correctly followed the prompt's unhappy-path
  branch (re-asks with the reference number once, then ends gracefully); disposition came back
  `{"DISPOSITION":"unclear","payout_date":"","reference_no":"CLM-2026-00417"}`. Note the gap: `reference_no` was
  populated even though the desk never confirmed it — it was pulled from the agent's own spoken question, not a
  fact the counterparty verified. Real limitation for Q4: extraction doesn't reliably distinguish "we said it" from
  "they confirmed it."
- Both webhook posts included a full timestamped transcript, `call_infra.call_status` (CDR-style), `rec_path`
  (present even for a chat-mode test, though no real audio exists for a chat call), `bot_type: "voice_outbound"`,
  `environment: "production"`, `mode: "BOT_TESTING"`.

**Conversation Flow tab — three features exist and are configurable (not just documented):**
- **Dynamic Messages** and **Pre-call Variables** toggles exist (not deep-tested this session).
- **Transfer to Agent** is a full feature, not just a checkbox: LLM-judged "Transfer Condition Prompt", one or more
  phone-number routes (static number or variable-based), a per-route "Routing Condition Prompt" and custom
  "Transfer Message", plus a "Send transcript on transfer" toggle to one or more destinations. Answers 10.5's open
  "transfer-to-human fallback" item: it exists and is reasonably rich.

**Languages (Agents workspace) — 12, wider than the APIs workspace's 10:** English (IN, primary), Hindi, Kannada,
Tamil, Telugu, Bengali, Gujarati, Malayalam, Marathi, Odia, Assamese, Urdu. Everything else (English US/AU/GB/PH,
Spanish, Punjabi, Italian, German, French, Filipino, Indonesian, Arabic, Japanese, Sinhala, Thai, Malay, Portuguese,
Swedish, Burmese, Danish, Dutch) is greyed out "Unsupported" in the picker.

**LLM Model tab:** four providers selectable — **Gnani** (default; models: Aion v3.2 "ultra low latency for Indic",
Evon v2.0, Evon v2.0 Fast [default], Evon v2.0 Ultra), **Deepseek**, **Google**, **Open AI**. Knowledge-base
attachment, temperature (0–1, default 0.5) and max-tokens (100–500, default 300) sliders sit alongside.

**Conversation Logs / Call Insights — richer than the webhook payload:** each test call gets a detail page with a
latency gauge (ms, colour-banded "Good"/etc.), "Reason of the call", auto-written "Result" and "Overview", a
"Resolution" status (e.g. "Resolved"), the Post Call Extraction V2 fields, and **per-message sentiment + emotion
tags** (e.g. "Positive" / "Trust") on the transcript. None of the sentiment/emotion/overview/resolution fields
appeared in the webhook payload — they are UI-only today. Answers 10.5's "Call Insights in webhook or UI only" item:
**both, but richer in the UI.**

**Actions / MCP Tools tab:** pre-built integrations for SMS (Twilio), CRM (Zoho), Ticketing (Zoho), Email
(MailChimp, SendGrid), plus a generic "Add Custom Integration" (Method + URL + key/value auth — a bare REST call the
agent can invoke) and a separate "MCP Tools" sub-tab (MCP server support at the account level too, under Manage →
Integrations → "Add MCP Server"). This is the mid-call tool-use path 10.5 could only read about from the docs.

**Manage section (account-level, not per-agent):** Integrations, Whitelisted, Inbound Numbers, Voice Library, Audit
Logs. **Inbound Numbers was empty with no visible self-serve "add number" flow** — inconclusive on native Indian
numbers vs. Twilio import; likely requires a sales/provisioning step not exposed in this UI. **Audit Logs page
exists but showed 0 logs** despite creating the agent, saving the config three times, and running two test calls in
this session — either it only tracks a narrower set of actions (e.g. integrations, whitelist changes) or there is a
lag; either way, "audit log" cannot be claimed as verified-working for agent-config changes.

**Voice Persona tab:** reusable named personas (voice, gender, TTS provider/rate), a "Caching" toggle (serves cached
audio for common phrases instead of regenerating — latency optimisation), and an "Ambient Sound" toggle. No
recording/retention toggle found anywhere in the agent config — recording behaviour remains undocumented-in-UI,
consistent with 10.5's "no retention, hash, signature" reading of the docs.

**Not tested this session (time-boxed):** a real outbound phone call via "Trigger Agent Call" (only chat-mode
tested), voice biometrics, campaigns/bulk dial, FAQ Answers tab, Transcriber tab detail, and the pre-call Dynamic
Messages 200/400 gate in practice.

**Real phone call, 25 Sep 2026 (evening):** the team placed a live call via Trigger Agent Call to a whitelisted phone and
played the desk. The call worked and appeared in the call logs; the team judged its behaviour fit for the design. Cost per
call, recording availability and the disposition values from the phone call were not written down.
On the real call, "we don't talk to bots" got the same result as chat test D: the agent said it is an AI calling on the
claimant's behalf, that someone would call back later and that it would notify them. It did not transfer.
