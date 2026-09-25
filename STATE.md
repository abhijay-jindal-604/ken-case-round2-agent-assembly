# State as of 25 Sep 2026

## Done
- Round 1 handover brief (`handover-brief/`).
- Round 2 context file: questions verbatim, judging, team, R1 answers, evidence, working map per question (§7).
- Rail docs read in full: Pine Labs (+Setu, P3P, Grantex), Gnani, Delhivery (+Maps); cross-rail summary with the
  gaps and the proposed Q3 state changes (§10.4).
- Gnani platform walkthrough, as far as the account allowed (§10.5): the Gnani APIs workspace works (STT Gnani Prisma
  V2.5, TTS Gnani Timbre v2.5 Beta, cloning, Rs 27/h STT, Rs 27 per 10k TTS chars, 60 req/min, 20 concurrent WS).
  Gnani Agents rejected a personal Gmail ("Unsupported Email Type"), so agent features were not verified via that account.

## Not started: the eight answers
1. Lock the Q3 state machine (from the §7 skeleton plus the §10.4 changes: S0 objects, S4 physical branch, S8
   submission vs completeness, S9 as a claim-state read, S11a/b/c, new unhappy branches).
2. Build the Q4 capability table against the Q3 state numbers (the load-bearing question).
3. Q1 + Q2, then Q5 (fourth rail; lead candidate: counterparty claim-state rail), Q6 (human interface), Q7 (name), Q8 (which Indian company).
4. Check the form's character limits; final pass for sameness with the AI baseline; attach the AI-conversation log link.

## Open items for the human
- Test Gnani agent access (the user reports agent calls partly working in another browser). Priority tests:
  1. Claim-status call: agent asks a desk for claim status, disposition emits JSON (status, payout_date, reference_no),
     post-call webhook to webhook.site; try normal, vague and contradictory answers; save payload.
  2. Pre-call gate (Dynamic Messages 200/400) exists in UI?
  3. Languages per agent, LLM list, recording on/off + retention + MP3, transfer-to-human fallback, Call Insights in webhook or UI only.
  4. Campaigns/bulk, production deployment requirements, Indian numbers in-app vs Twilio import, cost per call/minute.
  5. "After API Call Variables" working? Voice biometrics present?
- Paste into context §2: FAQ answers, "Getting your money back" opening text, Competition Updates, per-question character limits.
- Evidence: 2-3 short consented conversations (T&E claimant, finance/HR desk: do they still need physical originals?, health claimant).
- Optional: Delhivery Maps Address Verification screenshots; email lastmile-integration@delhivery.com.

## Open decisions (human)
- Q7 name: keep "Paid Tuesday" or rename.
- Accept the logistics revision (no role in the money; two bounded supporting uses) as a change from Round 1.
- Q5 pick and the Indian company that would build it.
- Q8 pick from the §7 candidates.

## Submission
Share the AI conversation log link(s); type answers into the form before 25 Sep 2026, 11:59 PM IST.
