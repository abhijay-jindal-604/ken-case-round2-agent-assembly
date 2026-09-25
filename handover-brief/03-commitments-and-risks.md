# Commitments, and the full-ambition version to build the next round around

This round (15 Sept–10 Oct) is **Product Strategy**: judges want a fully
specified build — complete flows, the segment map, the wall you hit and why —
not a working prototype. That means the constraint that actually governs this
file is "how good and how thorough is the plan," not "what can two students
literally stand up before 10 October." Don't let a build-time instinct scope
the mechanism down. If the plan needs a signed co-lending partner, an insurer
API, or a regulatory sandbox slot to be the *right* mechanism, specify that as
the plan — the wall is a deliverable to name precisely, not a reason to
retreat to a smaller idea before anyone asks.

The submission itself already did some of this retreating (the "concierge"
framing, "no partner is signed so we only do 20-25 hand-run claims"). That
text is public record and shouldn't be contradicted outright, but the next
round is the chance to build the ambitious version *on top of* it: show the
concierge run as the evidence-gathering step inside a much larger mechanism,
not as the ceiling of the idea.

## The full mechanism, undiminished

A claims-recovery-and-advance desk that pays any claimant — corporate T&E,
health insurance, any reimbursement with a published policy behind it —
70-95% of what they're owed within a day, underwritten off the document plus
the counterparty's own policy, no permission required from the counterparty
to start. It recovers from the payout. The full-scale version of this is a
lending business with a balance sheet, a licensed NBFC or co-lending
partnership, API-level integration into insurer/employer payout systems, and
a public settlement-speed board that becomes the reference dataset the whole
industry gets ranked against — the kind of thing that changes how insurers
price and how employers get chosen by candidates. That's the target to design
toward, not a stretch goal to footnote.

## What to actually build toward for 10 October — treat all of this as in scope

- **A real or realistically-modeled co-lending/licensing path.** Don't assume
  it away. Find out what an actual NBFC co-lending partnership requires,
  which real Indian NBFCs already do co-lending/factoring (there are several
  active in receivables financing), and specify who this could be signed
  with and on what terms — even if the actual signature doesn't happen by
  10 October, a credibly specific term sheet-shaped plan beats "not signed."
- **The 20-25 hand-run claims** are real evidence-gathering, not a ceiling —
  run them, and use them to argue the underwriting model works at any scale,
  not just to fill 25 rows.
- **The payee-side mandate** (Q5's missing Pine Labs capability) — go further
  than naming it. Spec the actual mandate flow, and push in the rails-round
  office hours for whether Pine Labs' P3P/Grantex team could actually support
  an inbound-payment assignment primitive. Ask them directly; don't assume
  the answer is no.
- **Insurer/employer cooperation** — the submission bet that zero signatures
  in 6-8 weeks is fine. For the strategy round, spec what changes once
  insurers *do* want in (API access, auto-honour, board placement as a
  competitive/marketing asset) — this is the expansion story judges will
  want on a Thoroughness-weighted rubric, not a hedge to avoid stating.
- **The regulatory question (NBFC/RBI co-lending rules)** — research it
  properly rather than parking it as a disclosed risk. Know the actual rules,
  cite the actual RBI circulars, and either show a compliant structure or
  show which regulatory sandbox program (IRDAI's included) could house this.

## The one number that still matters: the underwriting bet

> Gross recovery rate and net margin after write-offs and cost of capital.
> Target stated in the submission: **≥97% gross recovery at ≤8% claimant
> haircut.**

Use the 20-25 real claims to test this for real — but the answer to "what if
it's not profitable at first" is not "retreat to T+7," it's "what's the
actual underwriting model that gets this number up" (better document
classifiers, per-insurer/per-employer historical payout-speed priors, tiered
haircuts by claim risk, etc.). Solve the hard problem; don't pre-negotiate
down to the easy one.

## Rail fit — push these further, don't just restate them

- **Payments (Pine Labs).** Load-bearing and the declared rail to innovate
  on. Use the rails-round office hours to actually spec or prototype the
  payee-side inbound-assignment mandate against P3P/Grantex — this is the
  single highest-leverage thing to walk in with, since it's the exact gap
  named in the submission.
- **Voice (Gnani).** Real but secondary per the submission — worth actually
  wiring up for outbound recovery calls if it strengthens Thoroughness, not
  required to be central.
- **Logistics (Delhivery).** No honest fit — leave it out, that's not a
  scope-down, it's accuracy.

## Evidence base to build up, not just cite

The 3 doctor conversations and the IRDAI figures got the submission through
the written round. For the strategy round, go get more: more claimants,
more employers, an actual conversation with a co-lending NBFC or a
factoring company, actual conversation with Pine Labs about the mandate gap.
More evidence only strengthens the Evidence and Thoroughness scores — there's
no reason to stop at 3 conversations now that there's three-plus weeks
instead of three days.

## Open, unresolved — check status before planning

- Whether the 2026 judging panel has been announced since 9 September, and if
  so, its profile (operator/investor vs. academic/impact) — this should shape
  emphasis, not ambition.
- Whether the 10 October finale format (time limit, live vs. recorded) has
  been announced.
