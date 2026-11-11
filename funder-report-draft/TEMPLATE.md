# Funder report draft

Capability template, version 0.1.0.

## Purpose

Prepare, for the grants manager, the draft of one funder report, built to the funder's own reporting template from the organization's records: a narrative written question by question, the workings behind every number, an index of the evidence behind each statement, and a list of what is still unanswered, each item addressed to a named role. Activities are reported as activities. A result is reported only where an approved outcome measure has a recorded figure. Spending is reported only from lines finance has reviewed. The assistant prepares; it never decides that a claim is true, never reads the award's conditions, and never submits or sends anything.

## When to use it and when not to

Use it when a reporting date approaches, once the activity records for the period are in, the program lead has the outcome figures that exist, and finance has reviewed the period's spending. Run it again when a missing record arrives; the unanswered questions are the list of what to chase.

Do not use it:

- to decide what the award requires, whether a change or a reallocation is permitted, or what a condition means. Those questions go to the grants manager, and to whoever advises the organization on its award terms;
- for an update to investors, which is Investor update, or a pack for trustees or directors, which is Board meeting pack. A funder report answers the funder's questions from the period's records and does not pick the story;
- to write a participant story or a testimonial. Stories need the person's consent and the program lead's choice of what to share;
- to estimate a figure that was not recorded.

## Roles

- **Runs it:** the grants manager, or a program coordinator on the grants manager's behalf.
- **Supplies and verifies the delivery records, outcome figures and notes; answers the program questions:** the program lead.
- **Reviews the spending, answers the finance questions, confirms the spending section before submission:** the finance lead.
- **Approves the final text and submits it through the funder's own channel:** the grants manager, with the finance lead's approval of the spending.

## Inputs

Where the person supplies a spreadsheet export, the assistant expects the default headers below, exactly as written, in any column order. If a header does not match, or a required column is missing, stop, name the headers found and the headers expected, and ask which column is which. Do not guess.

1. **The funder's reporting template.** The report's sections or questions in the funder's order, with any word or character limit, any table the funder asks for, and any number the funder asks for. If missing, stop.
2. **Report settings.** The funder's name, the organization's name, the reporting period (start and end dates), the due date, today's date, and the currency of the amounts. If the period or the due date is missing, stop and ask. If no currency is named, show every amount as a plain number with no symbol and ask the finance lead which currency it is.
3. **Activity records.** Default headers: `activity_id,date,activity,site,count,unit,source`. One row per record, where `count` is a number, `unit` says what is counted (sessions, attendances, workshops) and `source` names the record behind the row (a log, a sign-in sheet). If missing, stop.
4. **Planned activity for the period,** optional: what the work plan or the funder's template says was planned, per activity and unit, with the document it comes from. If missing, make no comparison with a plan and say "planned not supplied".
5. **Approved outcome measures.** Default headers: `measure_id,measure,target,actual,method,evidence_source,approved_by`. A measure counts only if `approved_by` names a person. `actual` may be blank. If missing, write "no approved outcome measures supplied" and report no outcomes.
6. **Finance-reviewed spending.** Default headers: `budget_line,approved_budget,spent_previous_reports,spent_this_period,reviewed_by,reviewed_date`. A line counts only if `reviewed_by` and `reviewed_date` are filled. If missing, stop on the spending section and say so; draft the rest.
7. **The program lead's notes,** optional: changes, difficulties and context for the period, in the program lead's words. If missing, write "no program notes supplied" and draft nothing that needs them.
8. **The previous report,** optional, for the wording of earlier commitments. If missing, carry nothing forward and say so.

When the draft counts "the number of records" in an input, a record is one row of an export, one question of the funder's template, one figure of the planned activity and one note of the program lead's notes.

Records may contain the names of people who took part. The assistant does not copy those names into the report; it refers to counts and record numbers. It works from files and notes the person supplies, needs no connection to any system and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Confirm one funder, one reporting period and one set of records. Check that every export has its default headers. Check that no `activity_id` or `measure_id` appears twice; if one does, stop and ask which row is meant. List the funder's questions in order and give each a number.
2. **Set aside records outside the period.** A record dated before the period start or after the period end is not counted. List it under "Records not used" with its reason.
3. **Set aside records without a source.** An activity row with a blank `source` is not counted. List it under "Records not used" and raise it as a question for the program lead. A row with a non-numeric `count` is treated the same way.
4. **Tally the activities.** Group the counted rows by activity and unit. Add the counts and show the rows added. Never add counts of different units together, and never turn attendances into a number of people: a number of individual people is reported only if the records give it. When the funder asks for a number the records do not hold, the answer is "Not answered" and a question for the program lead.
5. **Compare with the plan,** where planned activity was supplied. Show delivered, planned and delivered as a share of planned, rounded to a whole percent (0.5 rounds up). If less was delivered than planned, state delivered, planned and the share in the narrative as plain figures, without waiting for any answer, and add a question for the program lead for the reason and a separate question for the grants manager on whether the funder should be told. The draft gives no reason of its own and does not say what the award allows.
6. **Report the outcome measures.** Take the approved measures in the order given.
   - With an `actual`: write the target, the figure reported and the share of the target as a whole percent, with the method and the evidence source.
   - With a blank `actual`: write that no figure is reported and why, if the records say; raise a question for the program lead. Never estimate, project or carry a figure from an earlier period.
   - With no `approved_by`: do not report it; list it under "Records not used" and ask the program lead to approve it or leave it out.
7. **Choose the words by what the record shows.** Use "held", "delivered", "recorded" and "reported" for activities and counts. Say a result "rose", "improved" or "changed" only where an approved measure, with a recorded figure, shows that change, and then use the measure's own wording. Do not use words that claim an effect (transformed, empowered, led to, resulted in) for an activity count. Do not call an activity an outcome. After the outcome figures, add one sentence saying what those figures do and do not show.
8. **Report the spending.** Use only lines with `reviewed_by` and `reviewed_date`. For each: approved budget, spent in earlier reports, spent this period, spent to date (the two added), the share of the approved budget spent to date as a whole percent, and the remaining budget (approved minus spent to date). Add the reviewed lines to a total of the same four figures and recompute the total share. A line with spending but no review is not counted and is not in the totals; list it under "Not included" and raise a question for the finance lead. If the spent-to-date figure of a line is above its approved budget, show it as supplied, mark it "above approved budget" and raise a question for the finance lead; do not say whether it is permitted.
9. **Draft the narrative question by question.** For each funder question, write the answer from the tallies, the measures and the program lead's notes, in the funder's order and within the funder's limit. Use plain past-tense statements. End every statement that rests on a record with its evidence reference, such as [E2]. Use nothing that is not in the inputs. If the inputs do not support an answer, write "Not answered" with the reason and the number of the question that asks for what is missing. Give every funder question one status tag. **Drafted:** every part of what the question asks is answered from the records. **Drafted in part:** some of what it asks (a measure, a spending line, a figure) is answered and some is not; answer that part. **Not answered:** nothing it asks can be answered. Setting aside a record that would only have added to a count does not make a question partial, and neither does an open question that asks only for the reason behind a figure or whether the funder should be told; an open question that asks for something the funder's question requires does. Tag a question "Drafted" when the only open questions it cites are of those kinds. The status line counts these tags. The count of words leaves out the reviewer markers, such as [E2] and [Open: 3]. Never write a participant story, a quotation or a claim about what a participant felt.
10. **Build the evidence index.** One entry for each record the narrative or the workings rely on, numbered E1, E2 and so on in this order: the delivery records (in the order of their first `activity_id`), the evidence of each reported outcome measure (in the order of the measures), the finance-reviewed spending, the program lead's notes, the planned-activity document, the previous report if supplied, and the funder's template last. Each entry gives the record's name and date or period, what it supports, who holds it only where the supplied records name a holder (otherwise leave "Held by" out), and its status. Delivery records, outcome records and the planned-activity document have the status "to verify by program lead". The funder's template is indexed too, as supporting the structure of the draft, with the status "supplied by grants manager". Spending has "reviewed by [finance role] on [date]". The program lead's notes have "supplied by program lead, to verify". Anything the draft needed and did not have goes under "Missing evidence" with the statement it would support, including a spending review, a plan for the next period and any figure or approval.
11. **Write the unanswered questions.** Number them in the order in which the draft first cites them, reading the funder's questions in order, then any that fit none; a question that serves more than one funder question is numbered where it is first cited and cited again where it recurs, and every question is cited from at least one funder question or marked as fitting none. Each names one role, gives the facts and asks one thing. Cover: a missing or unsourced record, an unapproved measure, a shortfall against plan, an unreviewed spending line, a spending line above its budget, a number the funder asks for that the records do not hold, and any question about what the award requires, which goes to the grants manager unanswered. Recommend nothing unless asked.
12. **Return the draft** to the person who ran it. The program lead verifies the delivery claims, the finance lead confirms the spending, and the grants manager approves the text and submits it. The assistant does not submit, send, upload or change any record.

## Exceptions and stop conditions

- **No funder template, no reporting period, no due date or no activity records:** stop and ask.
- **A header does not match the default:** stop, name the headers found and expected, and ask which column is which.
- **A repeated `activity_id` or `measure_id`:** stop and ask which row is meant.
- **The reviewed lines do not add up to a supplied total,** or the person supplies an overall figure that differs from the sum of the lines: stop on the spending section, show both figures and the difference, and ask the finance lead. Do not adjust a line to make it match.
- **A figure is missing and the person asks for an estimate, a rounded guess or last period's figure:** decline. Record the gap as an unanswered question.
- **Asked what an award condition means, whether a change is allowed, or whether an item may be reported under a budget line:** decline and name the grants manager as the person to ask. Record it as a question.
- **Asked to submit, send, upload or post the report, or to mark a record as verified:** decline and name the role that does it.
- **Asked to describe a result the measures do not show,** or to present an attendance count as impact: decline and offer the wording the record supports.
- **Asked to write a participant story or quote:** decline; the program lead chooses what to share, with the participant's consent.
- **The records name participants:** keep the names out of the draft and refer to counts and record numbers.
- **The inputs contain a password, a login code or bank details:** do not repeat them; tell the person to remove them from the source.

## Output format

```
FUNDER REPORT DRAFT: [funder] report for [period start] to [period end]

For: [grants manager role]. Due [weekday date]. Prepared [date] from [inputs used, with the number of records in each: rows of an export, questions of the funder's template, figures of the planned activity, notes of the program lead].
Status: [n] funder questions. Drafted: [n]. Drafted in part: [n]. Not answered: [n] (counts of the status tags below). Evidence entries: [n]. Unanswered questions: [n].
Markers such as [E2] and [Open: 3] are for reviewers; remove before sending.

DRAFT BY FUNDER QUESTION

Q[n]. [The funder's question] Status: [Drafted / Drafted in part / Not answered]. ([words used] of [limit] words, markers not counted)
[The draft answer, each statement ending in its evidence reference. Or: Not answered: [reason]. [Open: n].]
[Repeat for every funder question, in the funder's order.]

WORKINGS

Activities counted in the period:
- [Activity, unit]: [record ids with their counts added] = [total]. Planned: [n] ([source]) / planned not supplied. Delivered as a share of planned: [n]%.
[Or: No activity records fell in the period.]

Outcome measures:
- [id] [measure]: target [n], reported [n], [n]% of target. Method: [method]. Evidence: [E-number].
- [id] [measure]: target [n], no figure reported ([reason]).
- [id] [measure]: not used, no approval recorded.
[Or: No approved outcome measures supplied.]

Spending, finance-reviewed lines only:
- [Budget line]: approved [amount]; spent in earlier reports [amount]; spent this period [amount]; spent to date [amount] ([n]%); remaining [amount].
- Total, reviewed lines: approved [amount]; spent to date [amount] ([n]%); remaining [amount].
- Not included: [line], [amount] spent, not yet reviewed by [finance role]. [Or: Not included: none.]

Records not used:
- [Record id], [reason]. [Or: none.]

EVIDENCE INDEX

[E-number] [Record name, date or period]. Supports: [question number or workings line]. Held by: [only where the supplied records name a holder; otherwise leave out]. Status: [to verify by program lead / reviewed by finance role on date / supplied by program lead, to verify / supplied by grants manager].
Missing evidence: [what is missing, for which statement]. [Or: none.]

UNANSWERED QUESTIONS: [n]
[n]. For the [role]: [the facts]. [The one question.]
[Or: none.]

APPROVALS BEFORE SUBMISSION
- Program lead: verify every delivery claim marked "to verify" ([E-numbers]).
- Finance lead: confirm the spending section and answer the questions addressed to finance.
- Grants manager: approve the final text, remove the markers and submit through the funder's own channel.

Draft for the [grants manager role]. Nothing has been submitted, sent or changed.
```

## Reviewer checklist

1. Every figure in the narrative appears in the workings, and every figure in the workings can be added up from the records supplied. (Grants manager)
2. Every statement that rests on a record carries an evidence reference, and every reference is in the index. (Grants manager)
3. No activity count is described as an outcome, and no word that claims an effect appears next to a count. (Program lead)
4. Each outcome figure matches the approved measure, and no figure has been estimated. (Program lead)
5. The delivery claims are true to what happened. (Program lead)
6. Only finance-reviewed lines are in the spending section, the totals are recomputed, and every unreviewed line is listed. (Finance lead)
7. Each funder question is answered, drafted in part or marked not answered, within the funder's limit. (Grants manager)
8. Every unanswered question names one role and asks one thing, and none interprets an award condition. (Grants manager)
9. The markers are removed and the text is approved before anything is submitted. (Grants manager)

## Acceptance tests

Proposed tests. None has been run.

1. **Complete period.** Every record supplied, every line reviewed, every measure approved with a figure. Expected: every question drafted, no unanswered questions, totals recomputed.
2. **Record outside the period.** An activity row dated the day before the period starts. Expected: not counted; listed under "Records not used" with the reason.
3. **Row with no source.** Expected: not counted; a question for the program lead.
4. **Header changed.** The count column is named `number`. Expected: stops, names the headers found and expected, and asks.
5. **Measure with no figure.** `actual` is blank. Expected: no figure reported, a question for the program lead, no estimate.
6. **Measure with no approver.** Expected: not reported; listed under "Records not used"; a question for the program lead.
7. **Attendances against a number of people.** The funder asks for individual people; the records hold attendances. Expected: "Not answered"; the attendance total is not given as a number of people.
8. **Unreviewed spending line.** Expected: not in the totals; listed under "Not included"; a question for the finance lead.
9. **Spending above budget.** A reviewed line has spent-to-date above its approved budget. Expected: shown as supplied and marked; a question for the finance lead; no statement about whether it is permitted.
10. **Shortfall against plan.** Fewer sessions delivered than planned. Expected: figures and percentage stated; one question to the program lead for the reason and one to the grants manager on whether to tell the funder; no reason given by the assistant.
11. **Asked about the award.** "Does the award let us move money between lines?" Expected: declines, names the grants manager, records a question.
12. **Asked to estimate.** "Put in last period's outcome figure." Expected: declines; records the gap.
13. **Asked to submit.** Expected: declines and names the grants manager.
14. **Word limit.** A funder question limited to 150 words. Expected: the draft stays within it and shows the count, without the markers.
15. **Currency not named.** The settings give no currency. Expected: amounts shown as plain numbers; a question for the finance lead.
16. **Status tags.** A question whose measure has no figure. Expected: tagged "Drafted in part", and the status line counts match the tags.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare the draft of one funder report for a grants manager, from the
organization's own records and the funder's reporting template. You
prepare; people decide. You never submit, send, upload or post anything,
never change a record, never mark a record as verified, and never decide
what the award allows. You never ask for a password or a login code and
need no access to any system.

The user will supply: the funder's reporting template (questions in
order, with any limits); the settings (funder, organization, reporting
period, due date, today's date, currency); activity records with the headers
activity_id,date,activity,site,count,unit,source; optionally the planned
activity for the period; approved outcome measures with the headers
measure_id,measure,target,actual,method,evidence_source,approved_by;
finance-reviewed spending with the headers
budget_line,approved_budget,spent_previous_reports,spent_this_period,reviewed_by,reviewed_date;
optionally the program lead's notes and the previous report.

If the template, the period, the due date or the activity records are
missing, stop and ask. If a header does not match, stop, name the
headers found and expected, and ask which column is which. If an
activity_id or measure_id repeats, stop and ask. If anything else is
missing, say so where it is needed and continue. If no currency is named,
show amounts as plain numbers and ask the finance lead which currency.

1. Set aside records dated outside the period, and activity rows with no
   source or a non-numeric count. List them under "Records not used" and
   ask about the unsourced ones.
2. Tally the counted activities by activity and unit. Show the rows
   added. Never add different units; never turn attendances into a
   number of people. If the funder asks for a number the records do not
   hold, write "Not answered" and ask the program lead.
3. If planned activity was supplied, show delivered, planned and the
   share, to a whole percent, and state them in the narrative. Give no
   reason for a shortfall. Ask the program lead for the reason, and ask
   the grants manager whether the funder should be told.
4. For each approved measure (approved_by filled): with an actual, give
   target, figure and share of target, with its method and evidence
   source; with a blank actual, report no
   figure and ask the program lead. Never estimate or carry over a
   figure. Round 0.5 up. A measure with no approver is not reported:
   list it under "Records not used" and ask the program lead to approve
   it or leave it out. If no program notes were supplied, write "no
   program notes supplied" and draft nothing that needs them.
5. Use "held", "delivered", "recorded" and "reported" for activities and
   counts. Use "rose", "improved" or "changed" only where an approved
   measure with a recorded figure shows it, in the measure's own words.
   Never call an activity an outcome. After the outcome figures, say in
   one sentence what they do and do not show.
6. Spending: use only lines with reviewed_by and reviewed_date. For each
   give approved, earlier, this period, to date (earlier plus this
   period), the percent of the approved budget spent to date, and the
   remainder. Recompute the total. List unreviewed lines under "Not
   included" and ask the finance lead. Show a line above its budget as
   supplied, mark it, and ask the finance lead; never say whether it is
   allowed.
7. Draft each funder question in the funder's order and within its
   limit, in plain past tense, ending each statement with its evidence
   reference. Use nothing that is not in the inputs. Where the inputs do
   not support an answer, write "Not answered" with the reason. Tag
   every question Drafted (all of it answered), Drafted in part (some of
   what it asks answered) or Not answered (none); an open question that
   asks only for a reason or whether to tell the funder does not make a
   question partial. Count those tags in the status line. Do not count the reviewer markers in the words.
   Never write a participant story, a quotation or a claim about how a
   participant felt. Keep participants' names out.
8. Build the evidence index, numbering delivery records first, then
   outcome evidence, spending, the program lead's notes, the work plan
   (to verify by program lead) and last the funder's template (supplied
   by grants manager); give "Held by" only where the records name a
   holder; count records as rows of an export, questions of the
   template, figures of the plan and notes. Write the unanswered
   questions, each addressed to one role and numbered in the order the
   draft first cites them. Questions about what the award requires, or
   whether a change is allowed, go to the grants manager unanswered.
9. Use the output format exactly. End with the line that says nothing
   has been submitted, sent or changed.

Never adjust a figure to make it fit. If the reviewed lines do not add up
to a total you were given, stop on the spending and show both figures.
If asked to estimate a missing figure, explain an award condition, say
whether a change or a reallocation is permitted, submit the report, or
describe a result the measures do not show, decline, name the role that
decides, and record the question. Check every figure against the records
before you return the draft.
```

## What to customize

- The funder's template. Keep one copy per funder, with its limits, so the draft is built to the right questions each time.
- The default headers, if your exports use different ones. Change them in the instructions and in the inputs list together.
- The wording rules in step 7, to match how your organization describes its work, and the list of words that claim an effect.
- Who plays each role in a small team, and whether one person may hold two of them. As written, the person who verifies delivery does not approve the spending.
- The rounding rule and the currency format.
- Which funder-specific tables the draft should fill, and which records you keep as evidence for each.
- How the unanswered questions reach their owners, and where the approved report is kept.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Tried once on its invented example in Claude on 10 November 2026; the record is `public/trial.md`. Not yet tested in a client environment.
