# Funder report draft: an invented example

*Illustrative example with invented data.* The organization, the funder, the roles, the records and every figure below are invented. The organization is an invented small tutoring nonprofit, "Organization O", with a grants manager, a program lead and a finance lead. "Funder F" is an invented funder. First come the inputs the grants manager supplied, in full, then the draft the capability returned.

## The inputs

### 1. The funder's reporting template

```
Funder F, mid-year report. Answer in this order, within the limits.
Q1. Describe the activities delivered in the period. (250 words)
Q2. Report progress against each approved outcome measure. (200 words)
Q3. Report spending against the approved budget. (200 words)
Q4. Describe any challenges or changes to the plan. (150 words)
Q5. Describe your plans for the next period. (150 words)
Q6. How many individual students did the program reach? (a number)
```

### 2. Report settings

```
Funder: Funder F
Organization: Organization O
Reporting period: 1 April 2026 to 30 September 2026
Due: Friday 16 October 2026
Today: Monday 5 October 2026
Currency: US dollars
Roles: Grants manager, Program lead, Finance lead
```

### 3. Activity records

```
activity_id,date,activity,site,count,unit,source
A01,2026-04-30,After-school tutoring sessions held in April,Site 1,12,sessions,session log
A02,2026-05-31,After-school tutoring sessions held in May,Site 1,14,sessions,session log
A03,2026-06-30,After-school tutoring sessions held in June,Site 1,9,sessions,session log
A04,2026-09-30,After-school tutoring sessions held in September,Site 1,13,sessions,session log
A05,2026-04-30,Student attendances in April,Site 1,96,attendances,sign-in sheets
A06,2026-05-31,Student attendances in May,Site 1,118,attendances,sign-in sheets
A07,2026-06-30,Student attendances in June,Site 1,70,attendances,sign-in sheets
A08,2026-09-30,Student attendances in September,Site 1,104,attendances,sign-in sheets
A09,2026-05-20,Volunteer tutor training day,Site 1,11,volunteers trained,training sign-in
A10,2026-09-15,Family evening,Site 1,1,events,
A11,2026-03-28,After-school tutoring sessions held in March,Site 1,10,sessions,session log
```

### 4. Planned activity for the period

```
From the work plan: 52 after-school tutoring sessions planned for 1 April to 30 September 2026.
```

### 5. Approved outcome measures

```
measure_id,measure,target,actual,method,evidence_source,approved_by
M1,Students completing the spring reading check,40,36,Teacher-administered reading check,reading check results file,Program lead
M2,Students whose reading-check score rose between the first and last check,24,,Same check repeated in September,not yet collated,Program lead
M3,Volunteer tutors retained through the period,10,9,Volunteer register,volunteer register,Program lead
M4,Parents reporting improved reading confidence,30,27,Parent survey,survey summary,
```

### 6. Finance-reviewed spending

```
budget_line,approved_budget,spent_previous_reports,spent_this_period,reviewed_by,reviewed_date
Tutor stipends,30000,0,13200,Finance lead,2026-10-02
Materials and books,6000,0,2150,Finance lead,2026-10-02
Venue hire,8400,0,4200,Finance lead,2026-10-02
Volunteer training,2500,0,1100,Finance lead,2026-10-02
Evaluation and reporting,3600,0,900,,
```

### 7. The program lead's notes

```
- Summer break: no sessions in July or August, as agreed in the work plan.
- Site 1 moved rooms in May after the library closed its hall. Sessions continued.
- The September count includes a trial of Saturday sessions.
- The funder's form asks how many individual students we reached. We have not counted that yet.
```

No previous report was supplied.

## The output

```
FUNDER REPORT DRAFT: Funder F report for 1 April 2026 to 30 September 2026

For: Grants manager. Due Friday 16 October 2026. Prepared 5 October 2026 from the funder's template (6 questions), the activity records (11 rows), the planned activity (1 figure), the outcome measures (4 rows), the spending schedule (5 lines, 4 reviewed) and the program lead's notes (4 notes). No previous report supplied.
Status: 6 funder questions. Drafted: 2. Drafted in part: 2. Not answered: 2 (counts of the status tags below). Evidence entries: 9. Unanswered questions: 8.
Markers such as [E2] and [Open: 3] are for reviewers; remove before sending.

DRAFT BY FUNDER QUESTION

Q1. Describe the activities delivered in the period. Status: Drafted. (85 of 250 words, markers not counted)
Between 1 April and 30 September 2026 the project held 48 after-school tutoring sessions at Site 1 against 52 planned: 12 in April, 14 in May, 9 in June and 13 in September [E1] [E8]. No sessions ran in July or August, as agreed in the work plan [E7]. Students attended 388 times across the period: 96 in April, 118 in May, 70 in June and 104 in September [E2]. On 20 May the project held one training day, and eleven volunteer tutors were trained [E3]. [Open: 1, 2, 3]

Q2. Report progress against each approved outcome measure. Status: Drafted in part. (117 of 200 words, markers not counted)
Three approved measures are reported against; two have figures. Students completing the spring reading check: target 40, reported 36, which is 90% of target, by teacher-administered reading check, evidence in the reading check results file [E4]. Students whose reading-check score rose between the first and last check: target 24; the September results have not been collated, so no figure is reported [Open: 4]. Volunteer tutors retained through the period: target 10, reported 9, which is 90% of target, from the volunteer register [E5]. The reported figures record completion of the check and retention of tutors; they do not by themselves show a change in students' reading. A fourth measure has no recorded approval and is not reported [Open: 5].

Q3. Report spending against the approved budget. Status: Drafted in part. (67 of 200 words, markers not counted)
Spending on the four budget lines finance has reviewed totals $20,650 against $46,900 approved for those lines (44%), leaving $26,250 [E6]. Tutor stipends: $13,200 of $30,000 (44%). Materials and books: $2,150 of $6,000 (36%). Venue hire: $4,200 of $8,400 (50%). Volunteer training: $1,100 of $2,500 (44%). The evaluation and reporting line ($3,600 approved) is not included because its spending has not yet been reviewed by finance [Open: 6].

Q4. Describe any challenges or changes to the plan. Status: Drafted. (37 of 150 words, markers not counted)
Site 1 moved rooms in May after the library closed its hall; sessions continued [E7]. The September sessions include a trial of Saturday sessions [E7]. The project held 48 of 52 planned sessions, which is 92% [E1] [E8]. [Open: 2, 3]

Q5. Describe your plans for the next period. Status: Not answered. (0 of 150 words)
Not answered: no plan for the next period was supplied. [Open: 7]

Q6. How many individual students did the program reach? Status: Not answered. (a number)
Not answered: the records give 388 attendances, which are not a count of individual students. [Open: 8]

WORKINGS

Activities counted in the period:
- After-school tutoring sessions, sessions: A01 12 + A02 14 + A03 9 + A04 13 = 48. Planned: 52 (work plan). Delivered as a share of planned: 92%.
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
- A10, no source named for the family evening, so it is not counted.
- A11, dated 28 March 2026, before the period starts.
- M4, no approval recorded.

EVIDENCE INDEX

E1 Session log, April to June and September 2026 (A01 to A04). Supports: Q1, Q4, activity tally. Status: to verify by program lead.
E2 Sign-in sheets, April to June and September 2026 (A05 to A08). Supports: Q1, activity tally. Status: to verify by program lead.
E3 Volunteer tutor training sign-in, 20 May 2026 (A09). Supports: Q1, activity tally. Status: to verify by program lead.
E4 Reading check results file (M1). Supports: Q2, outcome measures. Status: to verify by program lead.
E5 Volunteer register (M3). Supports: Q2, outcome measures. Status: to verify by program lead.
E6 Finance-reviewed spending schedule, four lines. Supports: Q3, spending. Status: reviewed by Finance lead on 2 October 2026.
E7 Program lead's notes for the period. Supports: Q1, Q4. Status: supplied by program lead, to verify.
E8 Work plan, planned sessions for the period (52). Supports: Q1, Q4, activity tally. Status: to verify by program lead.
E9 Funder F's mid-year reporting template. Supports: the structure of the draft. Status: supplied by grants manager.
Missing evidence: the September reading-check results, for M2 (Q2); the approval of M4, if it is to be reported (Q2); finance's review of the evaluation and reporting line, for Q3; a plan for the next period, for Q5; a count of individual students, for Q6; the sign-in for the family evening, if it is to be reported (Q1).

UNANSWERED QUESTIONS: 8
1. For the Program lead: the family evening on 15 September (A10) has no source named, so it is not counted in Q1. Is there a sign-in or other record to name for it?
2. For the Program lead: 48 sessions were held against 52 planned, 92%, and no reason is in the notes. What was the reason?
3. For the Grants manager: sessions delivered were fewer than planned. Does the funder need to be told? The draft does not read the award terms.
4. For the Program lead: M2 has a target of 24 and no figure, because the September results are not yet collated. When will the figure be available, or is the measure to be reported as not yet available?
5. For the Program lead: M4 (parents reporting improved reading confidence) has a figure of 27 against a target of 30 and no approval recorded. Is it to be approved for this report or left out?
6. For the Finance lead: the evaluation and reporting line ($900 spent, $3,600 approved) has not been reviewed and is left out of Q3. Can it be reviewed before submission?
7. For the Program lead: the funder asks for plans for the next period (Q5) and none were supplied. What are they?
8. For the Program lead: the funder asks for the number of individual students reached (Q6). The records give attendances only. Can a count of individual students be made from the sign-in sheets?

APPROVALS BEFORE SUBMISSION
- Program lead: verify every delivery claim marked "to verify" (E1, E2, E3, E4, E5, E7, E8).
- Finance lead: confirm the spending section (E6) and answer question 6.
- Grants manager: answer question 3, approve the final text, remove the markers and submit through the funder's own channel.

Draft for the Grants manager. Nothing has been submitted, sent or changed.
```
