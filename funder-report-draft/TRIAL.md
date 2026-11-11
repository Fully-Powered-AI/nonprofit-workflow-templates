# Funder report draft: trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs were the invented example in `public/example.md` (Organization O, "Funder F", invented records and figures). No client data was used. This is the third run of the day. The first run, on the first version of the template, found gaps in it: no status tag on each question, no rule for stating a shortfall, no rule for numbering the unanswered questions, no status for the work plan or the funder's template, no currency, and no rule on whether the reviewer markers count towards a word limit. The template was revised and a second run followed it. That run left four points unsettled: what "Held by" holds when the records name only a kind of document, what counts as a record in the header, the order in which evidence entries are numbered, and whether an open question about a reason makes a question partial. An independent review raised the same points and others. The template was revised again (a record is defined; "Held by" is left out where no holder is named; the evidence entries have a fixed order; an open question that asks only for a reason does not make a question partial; the instruction block now says to list an unapproved measure under "Records not used" and ask the program lead, to round 0.5 up and to write "no program notes supplied"; the narrative now gives each measure's method), and the example's organization was renamed "Organization O". This run followed the twice-revised template. The earlier records are replaced by this one.

This run was not blind. It was done by the same model that revised the template, after it had read the earlier runs' output and the example's output. It shows that the revised instructions can be followed to a complete draft; it is not an independent test.

## Inputs used

The seven inputs in `public/example.md`: the funder's six-question template, the report settings (with the currency, US dollars), eleven activity records, the planned activity (52 sessions), four outcome measures, five spending lines and four program notes. No previous report.

## What came out

```
FUNDER REPORT DRAFT: Funder F report for 1 April 2026 to 30 September 2026

For: Grants manager. Due Friday 16 October 2026. Prepared 5 October 2026 from the funder's template (6 questions), the activity records (11 rows), planned activity (1 figure), the outcome measures (4 rows), the spending schedule (5 lines, 4 reviewed) and the program lead's notes (4 notes). No previous report supplied.
Status: 6 funder questions. Drafted: 2. Drafted in part: 2. Not answered: 2 (counts of the status tags below). Evidence entries: 9. Unanswered questions: 8.
Markers such as [E2] and [Open: 3] are for reviewers; remove before sending.

DRAFT BY FUNDER QUESTION

Q1. Describe the activities delivered in the period. Status: Drafted. (89 of 250 words, markers not counted)
Organization O held 48 after-school tutoring sessions at Site 1 against 52 planned (92%): 12 in April, 14 in May, 9 in June and 13 in September [E1] [E8]. No sessions were held in July or August, as agreed in the work plan [E7]. Student attendances recorded on sign-in sheets totalled 388: 96 in April, 118 in May, 70 in June and 104 in September [E2]. The September count includes a trial of Saturday sessions [E7]. Eleven volunteer tutors were trained at a training day on 20 May 2026 [E3]. [Open: 1, 2, 3]

Q2. Report progress against each approved outcome measure. Status: Drafted in part. (124 of 200 words, markers not counted)
Two of the three approved outcome measures have a recorded figure. M1, students completing the spring reading check: target 40, reported 36, 90% of target, by teacher-administered reading check, evidence in the reading check results file [E4]. M3, volunteer tutors retained through the period: target 10, reported 9, 90% of target, from the volunteer register [E5]. M2, students whose reading-check score rose between the first and last check: target 24; no figure is reported because the September check results have not yet been collated [Open: 4]. The reported figures show how many students completed the reading check and how many volunteer tutors stayed; they do not show a change in any student's reading. A fourth measure has no recorded approval and is not reported [Open: 5].

Q3. Report spending against the approved budget. Status: Drafted in part. (78 of 200 words, markers not counted)
Four budget lines have been reviewed by the Finance lead (2 October 2026) [E6]. Across them the approved budget is $46,900 and $20,650 has been spent to date (44%), leaving $26,250; nothing was spent in earlier reports. Tutor stipends: $13,200 of $30,000 (44%). Materials and books: $2,150 of $6,000 (36%). Venue hire: $4,200 of $8,400 (50%). Volunteer training: $1,100 of $2,500 (44%). The evaluation and reporting line is not included because finance has not yet reviewed it [Open: 6].

Q4. Describe any challenges or changes to the plan. Status: Drafted. (39 of 150 words, markers not counted)
Site 1 moved rooms in May after the library closed its hall, and sessions continued [E7]. A trial of Saturday sessions is included in the September count [E7]. The project held 48 of the 52 planned sessions, 92% [E1] [E8]. [Open: 2, 3]

Q5. Describe your plans for the next period. Status: Not answered. (0 of 150 words)
Not answered: no plan for the next period was supplied, and the program lead's notes do not describe one. [Open: 7]

Q6. How many individual students did the program reach? Status: Not answered. (a number)
Not answered: the records give 388 attendances, which are not a count of individual students, and the program lead's notes say students have not been counted yet. [Open: 8]

WORKINGS

Activities counted in the period:
- After-school tutoring sessions, sessions: A01 12 + A02 14 + A03 9 + A04 13 = 48. Planned: 52 (work plan) [E8]. Delivered as a share of planned: 92%.
- Student attendances, attendances: A05 96 + A06 118 + A07 70 + A08 104 = 388. Planned: not supplied.
- Volunteer tutor training day, volunteers trained: A09 11 = 11. Planned: not supplied.

Outcome measures:
- M1 Students completing the spring reading check: target 40, reported 36, 90% of target. Method: teacher-administered reading check. Evidence: E4.
- M2 Students whose reading-check score rose between the first and last check: target 24, no figure reported (the evidence source reads "not yet collated").
- M3 Volunteer tutors retained through the period: target 10, reported 9, 90% of target. Method: volunteer register. Evidence: E5.
- M4 Parents reporting improved reading confidence: not used, no approval recorded.

Spending, finance-reviewed lines only:
- Tutor stipends: approved $30,000; spent in earlier reports $0; spent this period $13,200; spent to date $13,200 (44%); remaining $16,800.
- Materials and books: approved $6,000; spent in earlier reports $0; spent this period $2,150; spent to date $2,150 (36%); remaining $3,850.
- Venue hire: approved $8,400; spent in earlier reports $0; spent this period $4,200; spent to date $4,200 (50%); remaining $4,200.
- Volunteer training: approved $2,500; spent in earlier reports $0; spent this period $1,100; spent to date $1,100 (44%); remaining $1,400.
- Total, reviewed lines: approved $46,900; spent to date $20,650 (44%); remaining $26,250.
- Not included: Evaluation and reporting, $900 spent, not yet reviewed by the Finance lead.

Records not used:
- A10, no source named, so not counted.
- A11, dated 28 March 2026, before the period starts.
- M4, no approval recorded.

EVIDENCE INDEX

E1 Session log, April to June and September 2026 (A01 to A04). Supports: Q1, Q4, activity tally. Status: to verify by program lead.
E2 Sign-in sheets, April to June and September 2026 (A05 to A08). Supports: Q1, activity tally. Status: to verify by program lead.
E3 Training sign-in, 20 May 2026 (A09). Supports: Q1, activity tally. Status: to verify by program lead.
E4 Reading check results file (M1). Supports: Q2, outcome measures. Status: to verify by program lead.
E5 Volunteer register (M3). Supports: Q2, outcome measures. Status: to verify by program lead.
E6 Finance-reviewed spending, four lines. Supports: Q3, spending. Status: reviewed by Finance lead on 2 October 2026.
E7 Program lead's notes for the period. Supports: Q1, Q4. Status: supplied by program lead, to verify.
E8 Work plan, 52 sessions planned for the period. Supports: Q1, Q4, activity tally. Status: to verify by program lead.
E9 Funder F's mid-year reporting template. Supports: the structure of the draft. Status: supplied by grants manager.
Missing evidence: a source for the family evening of 15 September, if it is to be reported (Q1); the September reading-check results for M2 (Q2); approval of M4 (Q2); finance's review of the evaluation and reporting line (Q3); the plan for the next period (Q5); a count of individual students (Q6).

UNANSWERED QUESTIONS: 8
1. For the Program lead: record A10, the family evening on 15 September, names no source, so it is not counted. Is there a record to name for it?
2. For the Program lead: 48 sessions were held against 52 planned, 92%, and the notes give no reason. What was the reason?
3. For the Grants manager: fewer sessions were delivered than planned (48 of 52). Should the funder be told? The draft does not read the award's terms.
4. For the Program lead: M2 has a target of 24 and no figure; its evidence source reads "not yet collated". When will the September results be collated and the figure be available?
5. For the Program lead: M4 (parents reporting improved reading confidence, target 30, actual 27) has no approval recorded. Is it to be approved for this report or left out?
6. For the Finance lead: the evaluation and reporting line ($900 spent, $3,600 approved) has no review and is left out of Q3. Can it be reviewed before submission?
7. For the Program lead: Q5 asks for plans for the next period and none were supplied. What are they?
8. For the Program lead: Q6 asks for the number of individual students reached and the records hold attendances only. Can a count of individual students be made from the sign-in sheets?

APPROVALS BEFORE SUBMISSION
- Program lead: verify every delivery claim marked "to verify" (E1, E2, E3, E4, E5, E7, E8).
- Finance lead: confirm the spending section and answer the questions addressed to finance.
- Grants manager: approve the final text, remove the markers and submit through the funder's own channel.

Draft for the Grants manager. Nothing has been submitted, sent or changed.
```

Word counts exclude the bracketed markers, as the template now says.

## What was observed

Every part of the output format was produced: the header and status line, six answers in the funder's order each with a status tag, the workings, the evidence index with missing evidence, eight numbered questions, the approvals block and the closing line. No stop condition fired: headers matched, no id repeated, and the template, period, due date, currency and activity records were all present. Nothing in the inputs asked the draft to decline anything.

The template did its main jobs. A11 (before the period) and A10 (no source) were set aside and listed. M4 (no approver) was not reported. The unreviewed evaluation line was left out of the totals. Attendances (388) were not turned into a number of students, and Q6 was marked not answered. M2 had no figure and none was estimated. The shortfall (48 of 52, 92%) was stated in the narrative and produced one question for the program lead and one for the grants manager, with no reason given by the draft. Every figure was recomputed from the rows; I found no arithmetic that needed correcting.

The revisions worked as intended:

- The status tags can be counted. Q1 and Q4 are drafted, Q2 (M2 has no figure) and Q3 (one line unreviewed) are drafted in part, and Q5 and Q6 are not answered, so the status line reads 2, 2 and 2. Q1 and Q4 cite open questions that ask only for a reason or whether to tell the funder (2 and 3), and the template's rule kept them as drafted without a choice.
- The evidence entries followed the fixed order without a choice: the three delivery records, the two outcome records, the spending, the notes, the work plan and the funder's template. The numbering now matches the published example.
- No "Held by" was written, because the records name no holder; this left each entry shorter and nothing was lost.
- The header counted records by the template's definition: 6 questions, 11 rows, 1 figure, 4 rows, 5 lines (4 reviewed) and 4 notes.
- The unanswered questions are numbered in the order the draft first cites them, and each is cited from at least one funder question: Q1 cites 1, 2 and 3, Q2 cites 4 and 5, Q3 cites 6, Q4 cites 2 and 3 again, Q5 cites 7, Q6 cites 8.
- Each reported measure carries its method and evidence source in the narrative as well as in the workings.
- With the currency named, amounts carry the dollar sign and are traceable to the settings.

Differences from the published example, all in wording rather than substance: the narrative differs in several places, so the word counts differ (89, 124, 78 and 39 here against 85, 117, 67 and 37 in the example). The example's text and this output were both written after the same revision, so they are close; that is a reason to read the example as a worked example and this record as one run, not as two independent ones.

Places where the template may still be unsettled, found in this run:

- **A fact only the notes report.** The statement that no sessions ran in July or August "as agreed in the work plan" comes from the program lead's notes, so I cited the notes [E7], not the work plan.
- **A set-aside record in Q1.** I treated the unsourced family evening as not making Q1 partial, following the template's rule that setting aside a record which would only have added to a count does not. A reviewer might read it differently.
- **The rule on reasons.** Q4 asks for challenges, and the shortfall is a challenge; I treated the open questions about its reason and about telling the funder as not making Q4 partial, following the new rule. A reviewer who reads the reason as part of what Q4 asks would tag it "Drafted in part".

Facts in the output that are not in the inputs: I found none. "Eleven volunteer tutors were trained" traces to A09 ("volunteers trained", 11).

This was one run on one invented example, not independently reviewed. It says nothing about how the template performs on a real funder's template or real records.
