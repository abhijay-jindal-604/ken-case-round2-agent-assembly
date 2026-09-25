# State as of 25 Sep 2026 (night): Round 2 SUBMITTED

## Round 2: submitted (25 Sep 2026, before 11:59 PM IST)
- Final answers are in `round2/03-answers.md`. The form text was pasted from chat versions of it. Differences:
  - All answers say "our agent". The name **Pehle** appears only in Q7.
  - Q3 was submitted as plain-text lists, not tables and ASCII art. The diagram link was optional.
  - Q4 was submitted as 33 template blocks (Name / Used at / Rail / ... / Build Status). The Build Status line uses
    only Exists or Must Build. Partial rows are "Must Build (partial: ...)". The "move_money: No role" row was
    folded into the Logistics heading. Off-rail items were an optional closing line.
  - Q8 wording was softened to "no longer runs employers' expense software", since only the Happay sale is verified.
- AI log link submitted: a Google Drive folder
  (https://drive.google.com/drive/folders/112DDvJr1CqbUF8an8vNVys7wMmLlGQg3), which should hold the Claude Code
  transcript and the Gnani test logs. The Gnani chat-demo link was suggested alongside it.
- GitHub push (https://github.com/abhijay-jindal-604/ken-case-round2-agent-assembly): the user does it manually. The
  Claude push was blocked. Not confirmed done. The local clone is in the old session scratchpad (commit 4d59771).

## Decisions (user)
- Q7: rename. The name was delegated to Claude, which picked **Pehle**; the product stays Paid Tuesday.
- Logistics revision accepted: Delhivery has no role in the money; two bounded uses (originals pickup, proof of delivery).
- Q5: counterparty claim-state rail, built by Setu.
- Q8: CRED.
- The form showed no character limits.

## Design calls (Claude, accepted)
- L3, not L4. The money acts sit inside limits the lender and claimant set.
- The advance is non-recourse on the counterparty's decision and full-recourse on the claimant's own acts.
- The auto-accept band is set once at signup.

## Evidence collected
- 8 Gnani chat tests: 6 pass, 1 partial, 1 fail (§10.5b).
- §10.6, from Bhaskar: webhook and disposition verified; Transfer to Agent exists; the extraction filled
  `reference_no` from our own words (hence U8b); Audit Logs empty; 12 languages.
- A real phone call (25 Sep) to a whitelisted phone worked and appeared in the call logs. "We don't talk to bots" gave a
  callback promise and no transfer, the same as in chat. Not recorded: cost per call, recording availability, the
  disposition JSON from the phone call.

## If we reach the next round
- Open items: configure Transfer to Agent routing to a real ops number and retest; cost per call; recording and
  retention; whether Delhivery allows medical papers [CHECK]; a Q3 diagram as a proper page.
- Context lives in `round2/00-round2-context.md`; answers in `round2/03-answers.md`.
