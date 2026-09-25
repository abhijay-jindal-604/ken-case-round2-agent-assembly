Continue the Ken Case Competition 2026 Round 2 ("Agent Assembly") work. Deadline: TODAY, Fri 25 Sep 2026, 11:59 PM IST.

Read first:
- /home/aj/Desktop/everything/hackathons/kenCase/round2/00-round2-context.md: the master context. It has the 8 questions verbatim, the judging, the Round 1 answers, the rail research (§10.1 Pine Labs, §10.2 Gnani docs, §10.3 Delhivery, §10.4 cross-rail summary and proposed Q3 state changes), the Gnani platform walkthrough (§10.5) and the Gnani agent chat tests (§10.5b).
- /home/aj/Desktop/everything/hackathons/kenCase/round2/01-todo-for-you.md: items only I can do.
- /home/aj/Desktop/everything/hackathons/kenCase/STATE.md: done and left.

Where things stand:
- Research is done. None of the 8 answers is drafted yet.
- Gnani: my personal Gmail is blocked from Gnani Agents. The Gnani APIs workspace (STT/TTS) works.
- I have agent access through another account. The agent "Paid Tuesday" (claim-status caller, test claim CLM-48213 for Asha Verma, ₹18450) has a shareable chat-demo link: https://app.gnani.ai/agents/chat-demo/e1adb832-479d-40f4-b08f-5e281ea806f0 . The Playwright browser can drive it. Wait for the greeting before typing. The input is iframe[title="Chat Widget"] with placeholder "Message".
- Chat test results (§10.5b): 6 pass, 1 partial (a vague "we'll look into it" makes it wait instead of asking for a date), and 1 fail. When the desk says "we don't talk to bots", a canned platform handoff overrides the prompt, promises a callback and ends the chat.
- Not yet verified: a real phone call, the disposition JSON, the post-call webhook payload, the recording, and cost per call.
- Public repo https://github.com/abhijay-jindal-604/ken-case-round2-agent-assembly holds the docs as of before the §10.5b chat tests. The local folder is not a git repo, so to update the repo, clone it, copy the files in, commit and push. Exclude the organisers' PDF, .playwright-mcp/, and screenshots or snapshots that show my email.

Next steps, in order:
1. Ask me for the four decisions if I haven't given them:
   - Q7 name: keep "Paid Tuesday" or rename.
   - Whether to accept the logistics revision (no role in the money; two bounded supporting uses).
   - Q5 fourth rail (lead candidate: the counterparty claim-state rail) and which Indian company should build it.
   - Q8 pick from the §7 candidates.
2. Lock the Q3 state machine from the §7 skeleton plus the §10.4 changes and the §10.5b findings:
   - S9's voice read stays unconfirmed until the money reconciles.
   - A contradiction goes to human review.
   - "Don't talk to bots" creates a human task.
   - A vague answer schedules a re-chase.
3. Build the Q4 capability table against the Q3 state numbers, using the §10 candidate rows. Mark each capability as verified, documented-only or must-build.
4. Draft Q1, Q2, Q5, Q6, Q7 and Q8. Fit the form's character limits (ask me for them). Do a pass to remove anything that sounds like a generic AI answer. Keep my decisions visible, because the judges grade human versus AI contributions.
5. Optionally, if I make a real Gnani call, log the webhook payload, cost and recording in §10.5b.
6. Push the final state to the repo.
