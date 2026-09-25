# Submitted answers — 10 September 2026

This is the exact text submitted to the portal for opening 14, "Getting your
money back," under the working title "Paid Tuesday." Treat this as public
record — the next round should build on it or honestly revise specific
claims, but should not silently contradict it.

---

## 01 — Who is this team, and why is this opening yours?

**Abhijay Jindal** — grew up watching this failure mode from the inside: both
parents are doctors, and my father is a spine surgeon and orthopaedician. I've
watched patients get claims denied for reasons that have nothing to do with
their treatment — an insurer demands an X-ray my father's own orthopaedic
evaluation never required, or a patient who got a surgery at a discount is
accused of double-dipping insurance and treated as fraud. The money lost isn't
one dramatic case — it's constant, small, and normalized enough that the
doctors around me can't even name a single instance because there are too
many.

**Bhaskar Kumar Arya** — watched a close friend's MRI claim get denied over a
pre-approval technicality: the scan itself was clinically warranted, but the
insurer's prior-authorization step wasn't cleared before the procedure, and an
out-of-pocket cost that runs into thousands became unrecoverable after the
fact, not because the claim was invalid but because of when the paperwork
happened.

**As a team (50 words):** Between us we've watched this failure from both
ends: Abhijay from years of proximity to a spine surgeon practising at
GMCH-32, a government hospital, Bhaskar from a friend's denied MRI claim. We
validated the pattern with 3 practising doctors (1 government setting, 2
private) before submitting: documentation-technicality and pre-approval-timing
denials came up unprompted in every conversation.

## 02 — The one customer insight you discovered.

Claimants lose before the clock starts. The people we spoke to described
resubmission loops — an unstamped bill, a missing summary — that occur before
a claim counts as filed. IRDAI reports 99.93% of health claims settled within
three months; that clock begins at complete filing. So our advance triggers on
the unfiled bill, not the filed claim.

**Attached:** `q2-interview-notes.md` (see `02-evidence-and-sources.md` in
this folder) — working notes from 3 doctor conversations (1 government
setting at GMCH-32, 2 private), early September 2026, written up afterward
(not a live transcript/recording, labeled as such), plus cited IRDAI figures
(via Business Standard/Business Today) on FY24 claim denial rates as
market-level context, not primary research. No audio/photo/survey attachment
was included — none existed, and none was fabricated.

## 03 — How your agent works, in six steps.

| # | Step | |
|---|---|---|
| 1 | **Trigger** | You forward one expense inbox or statement; we find money you never filed. |
| 2 | **What it knows** | Your employer's published T&E policy, and how fast that employer has paid us before. |
| 3 | **What it does** | Assembles the complete packet, advances 70–95% same day, then files and chases. |
| 4 | **Who it deals with** | The employer's finance desk, in our own name, under your one-time signed mandate. |
| 5 | **What it asks you** | Only at signup, then again only for facts a query needs from you. |
| 6 | **How it knows it's done** | The payout lands and reconciles to the rupee against what we advanced. |

## 04 — How your solution touches each rail.

**Payments — load-bearing.** Payments *is* the product: the advance out, the
recovery in, and a claimant-signed disbursement mandate with an auditable
trail, which is precisely the object Pine Labs' P3P and Grantex already
model.

**Logistics — no role, honestly.** Every claim we touch is documents and
money; the one physical leg in this opening, the return pickup, is a use-case
we deliberately excluded, so naming Delhivery here would be box-ticking.

**Voice — real but secondary.** Recovery is conducted by phone against finance
desks and TPAs in Indian languages, which is a genuine Gnani fit, but it
lowers our cost per recovery rather than carrying the mechanism.

## 05 — Which rail will you innovate on?

**Selected: Payments.** Missing: a payee-side mandate — the claimant
authorising, once, that a specific incoming reimbursement be routed to their
financing agent. Every Indian mandate today is a pull instrument on debits;
nothing lets a person assign an inbound payment.

## 06 — Which customer asset will you ask for?

Read access to their expense inbox and card/UPI statement. It's the only way
we find money they haven't filed — and they're paid before they file
anything.

## 07 — The annexation: which use-case do you subsume next?

Post-discharge health reimbursement claims. ClaimBuddy owns them at
admission, inside partner hospitals; nobody serves the person already home
with the bills. We arrive with the payout-speed data and the cash.

## 08 — Which of the sixteen openings would you never hand to an assistant?

**16 — Sticking to the goal.** A flawless assistant would hit the target on
your behalf, and the whole value of that opening is that the person did it
themselves — delegate it and there is nothing left to have kept.

## 09 — Which Indian company should have built this already?

**RazorpayX.** It runs payroll and expense disbursement for thousands of
employers, so it sees the reimbursement run, holds the employee's account,
and already moves money on payday. It hasn't built this because its customer
is the employer: advancing against an employer's unpaid reimbursement means
underwriting your own paying client's slowness, plus lending risk a payments
company won't hold.

## 10 — Which track are you entering?

**Selected: Product Strategy.**

We pick Strategy because the wall is the deliverable. Paid Tuesday advances a
claimant 70–95% of a stuck or unfiled reimbursement within a day,
underwritten off the document plus the counterparty's own published policy —
no employer or insurer agreement — and recovers from the payout. Three things
about that we specified rather than pretended away:

**The wall.** No licensed co-lending partner and no first-loss capital pool
can exist between 15 September and 10 October. We originate and service
only; the balance sheet sits with a licensed partner from day one, and that
partner is not signed. So the build round delivers the concierge version:
20–25 real stuck claims hand-run, each underwritten manually against a
published policy, each recovery reconciled — presented as the first 25 rows
of the settlement-speed board. Committed to now so it isn't discovered as a
retreat in October.

**The hard bet, unhedged.** Can we judge "policy-valid, will be paid" well
enough to advance same-day and not go broke? Not across all claim types. We
start with the one archetype that underwrites cleanly — salaried T&E against
a published corporate policy, which is also where our evidence sits. The
metric is gross recovery and net margin after write-offs, target ≥97%
recovery at ≤8% claimant haircut. Negative, and we narrow further or move to
T+7.

**The segment map runs the other way from the pitch.** The validated wedge is
corporate reimbursement backlogs; large insurance claims are the annexation
(Q7), not the proof. The by-product is the same in both: every advance is a
dated outflow, every recovery a dated reconciled inflow, so our own audited
book becomes a transaction-verified record of how fast each employer and
insurer actually pays. That board needs no counterparty's permission to
exist — insurer API access and auto-honour would move a counterparty up it,
and we expect zero signatures in the first eight weeks.
