# State as of 25 Sep 2026

## Done
- Round 1 handover brief (`handover-brief/`).
- Round 2 context file: questions verbatim, judging, team, R1 answers, evidence, working map per question (§7).
- Rail docs read in full: Pine Labs (+Setu, P3P, Grantex), Gnani, Delhivery (+Maps); cross-rail summary with the
  gaps and the proposed Q3 state changes (§10.4).
- Gnani platform walkthrough, as far as the account allowed (§10.5): the Gnani APIs workspace works (STT Gnani Prisma
  V2.5, TTS Gnani Timbre v2.5 Beta, cloning, Rs 27/h STT, Rs 27 per 10k TTS chars, 60 req/min, 20 concurrent WS).
  Gnani Agents rejected a personal Gmail ("Unsupported Email Type"), so agent features were not verified via that account.
- Gnani Agents unblocked with an official email; live-tested end to end (§10.6). Built and ran a real "claim status
  check" agent via the in-browser chat test mode, twice (clear answer + vague/unclear answer). Disposition extraction
  and the post-call webhook both verified working against webhook.site: `disposition_result` /
  `post_call_extraction_v2` came back correctly structured both times, including the `unclear` branch. Also confirmed:
  Transfer-to-Agent (real feature, not just a toggle), 12 supported languages, 4 LLM providers (Gnani/Deepseek/
  Google/OpenAI), rich Conversation Logs (latency, sentiment, emotion, auto-summary — richer than the webhook),
  Actions/MCP Tools (Twilio/Zoho/MailChimp/SendGrid prebuilt + custom REST integration + MCP server support). Gaps
  found: Audit Logs page exists but logged 0 entries for our session's agent creation/saves/test calls; Inbound
  Numbers had no visible self-serve "add number" flow; no recording/retention toggle found anywhere in the agent
  config. Not tested: real phone call (only chat-mode), voice biometrics, campaigns/bulk dial.

## Not started: the eight answers
1. Lock the Q3 state machine (from the §7 skeleton plus the §10.4 changes: S0 objects, S4 physical branch, S8
   submission vs completeness, S9 as a claim-state read, S11a/b/c, new unhappy branches).
2. Build the Q4 capability table against the Q3 state numbers (the load-bearing question).
3. Q1 + Q2, then Q5 (fourth rail; lead candidate: counterparty claim-state rail), Q6 (human interface), Q7 (name), Q8 (which Indian company).
4. Check the form's character limits; final pass for sameness with the AI baseline; attach the AI-conversation log link.

## Open items for the human
- Gnani Agents walkthrough done (§10.6) — see "Not tested" list there for what's left if there's time: a real phone
  call via Trigger Agent Call (only chat-mode tested), voice biometrics, campaigns/bulk dial, the pre-call Dynamic
  Messages 200/400 gate in practice, FAQ Answers tab, Transcriber tab detail, cost-per-minute for a real voice call
  (chat-mode test cost ~0.47 credits each, but that's not the same meter as a phone call).
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
