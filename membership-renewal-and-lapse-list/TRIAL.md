# Membership renewal and lapse list: trial on the example

- **Product:** Claude, run in Claude Code

Model: Claude Sonnet 5.5 (model ID claude-sonnet-5-5). Date of the run: 2026-11-19.

The inputs were the example for this template and nothing else. No client data was used. The inputs are the member export, renewal rules, approved facts and today's date in the "The inputs" section of [example.md](example.md): fifteen illustrative members of an illustrative arts association, with its organization name and two subject lines among the renewal rules, today 2026-11-02, last run 2026-10-01, a 30-day window and a 30-day grace period. This is the second run. The first run, on the same date, used the earlier inputs and instruction block; its record was replaced by this one because the example's inputs and the instruction block were then edited (an organization name and two subject lines were added to the renewal rules, and some wording was made explicit). This run followed the edited instruction block and output format. Unlike the first run, the model had already read the published output before producing its own, so this run is not blind; it was worked through row by row from the inputs and then compared with the published output.

## What came out

All eight sections, the totals line and the closing check lines were produced.

- Totals: export rows 15 = Due, reminder 3 + Due, auto-renew on 1 + In the grace period 2 + Lapsed since the last run 2 + Lapsed before the last run 1 + Not yet due 2 + Cancelled 1 + Records to check 3. The groups add back to 15.
- Due, reminder: M-1001 (Individual, email), M-1003 (Supporter, post), M-1009 (Household, marked do not contact: no message).
- Due, auto-renew on: M-1002, no reminder.
- Grace period: M-1004 (open until 2026-11-14, phone: use the draft as call notes) and M-1005 (open until 2026-11-19, with the note that auto-renew is on but the renewal date has passed).
- Lapsed since the last run: M-1006 (lapsed 2026-10-13, status lapsed) and M-1007 (lapsed 2026-10-06, with the note "still marked active in the system").
- Records to check, nothing drafted: M-1012 (renewal_date blank), M-1013 (2026-11-31 is not a real date), M-1015 (payment recorded 2026-10-29, after the renewal date of 2026-10-28, so the member may already have renewed).
- Left out: M-1009 (do not contact), M-1014 (cancelled), M-1008 (lapsed before the last run, on 2026-09-10), and two members not yet due, counted only.
- Renewal reminders: one each for Individual (with a due sentence and a grace sentence, each marked), Household (grace sentence only, for M-1005, with the auto-renew note to check first) and Supporter (due sentence only). Each used the subject line from the renewal rules and the fee, includes, renewal and questions sentences word for word, and was signed by Rosalind Kerr.
- Lapsed notes: Individual (signed by Rosalind Kerr) and Supporter (signed by Mateo Ferris, Chair), each with the lapsed-notes subject line from the renewal rules, the welcome-back line, the fee and includes sentences, the rejoin sentence and the questions line. A one-line statement that Household needed none.
- Check lines: every fact in the drafts is from the approved facts; no draft goes to a member marked do not contact.

## What was observed

Against the published output:

- The date groups, counts, dates, notes, records to check, left-out list, signers, subject lines and draft wording were the same. No member was placed in a different group. The heading and the subject lines now come from the organization name and subject lines in the inputs, not from the example's descriptive text.
- The template's own reviewer checklist passed on this run: the totals line adds up to 15; three rows spot-checked by hand (M-1004, M-1006, M-1008) fall in the right groups; nobody marked do not contact, cancelled or lapsed before the last run has a draft; each record to check names its field and the problem; each draft matches the approved sentences; signers match the rules; no draft singles out a member.
- Nothing in the output is a fact that is not in the inputs.
- Nothing made the run stop. No header mismatch, duplicate member_id, missing date, missing signer, missing subject line or missing approved facts arose, so those stop conditions were not exercised by this run. The ten acceptance tests in the template are still proposed, not run.

Points the first run found that the template now settles in words, none of which arose as a different result here: the source of the subject lines and the organization name, drafting for a grace-period member with auto-renew on, the exact due and grace sentences inside the instruction block, a member whose lapse date equals the last run's date (counted as lapsed before the last run), and a row that is both a record to check and marked do not contact (kept in Records to check and also named under Left out). The cases of equal dates and of a row with both conditions did not occur in the example, so those two rules were written down but not exercised.

This is one run on an example, and it was not blind. It shows the instructions produce a complete and consistent list when the inputs are clean. It does not show how the template behaves on a real export.

After this run, and without a further run, the template was edited in small ways that the example's inputs and the output recorded above do not exercise: a member marked lapsed whose renewal date equals today now goes to Records to check; a member who lapsed before the last run but is still marked active now carries a note under Left out; the For line of each drafted reminder is now specified to carry (due) or (grace), as the published example already shows; and the note wording is stated in the instruction block. None of these changes the recorded output for the example, and none has been run.
