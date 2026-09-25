# State as of 25 Sep 2026 (evening)

## Done
- Round 1 handover brief (`handover-brief/`).
- Round 2 context file (`round2/00-round2-context.md`): questions, judging, R1 answers, rail research (§10.1–§10.4),
  Gnani walkthrough (§10.5) and agent chat tests (§10.5b).
- Decisions (25 Sep):
  - Q7: rename. The name was delegated to Claude, which picked **Pehle**; the product stays Paid Tuesday.
  - Logistics revision: accepted.
  - Q5: claim-state rail, to be built by Setu.
  - Q8: CRED.
  - The form shows no character limits.
- **All 8 answers drafted: `round2/03-answers.md`.** It contains the Q3 state machine (S0–S13, U1–U19) and the Q4
  table tied to state numbers, with verified, documented-only and must-build marked.
- Web-checked: Happay's travel-and-expense business was sold to MakeMyTrip in Nov 2024, so Q8 was rewritten around
  this. CRED owns NewTap Finance (an NBFC) and co-lends CRED Cash with L&T Finance. NHCX routes claims between
  hospitals and payers and has been live since Jun 2024.

- Merged Bhaskar's §10.6 (commit 4d59771): verified the disposition JSON, the webhook and Transfer to Agent; 12 agent
  languages; Audit Logs empty. Q4/Q3/Q6 were updated from it (new U8b: a field only we said is dropped).

## Design calls made while drafting (review)
- Q2 is scored L3 (the money acts sit inside limits the lender and claimant set), not L4.
- The advance is non-recourse on the counterparty's decision and full-recourse on the claimant's own acts.
- The claimant sets an auto-accept band once at signup, which keeps R1's "asks only at signup".

## Left (human)
- Read `round2/03-answers.md`, change anything, then type it into the form before 11:59 PM IST.
- Share the AI conversation log link(s).
- Optional: a real Gnani phone call, to log the disposition JSON, webhook, recording and cost in §10.5b.
