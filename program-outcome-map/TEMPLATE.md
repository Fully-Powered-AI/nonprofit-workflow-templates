# Program outcome map

Capability template, version 0.1.0.

## Purpose

Prepare, before an evaluation, one map that links each activity of a program to the outcome it is meant to serve, from the program's own plan, measures and approved feedback. For each link the map shows the measures already held, the measures worth proposing, where the data comes from, the assumption that has to hold, what the evidence behind the link actually is, and the numbered questions that evidence cannot answer. The assistant prepares; it never claims an impact, never decides whether any person is eligible for help, never approves a measure, never collects data and never changes a record.

## When to use it and when not to

Use it when an evaluation, a funder review or a redesign is coming and the program and evaluation leads want to agree what is being tested before more data is collected. Run it again when an outcome is reworded, a measure is added or new figures arrive.

Do not use it:

- to plan the questions to put to a particular dataset, which is the work of analysis plan;
- to report a fixed set of measures month by month, which is the work of operations KPI scorecard;
- to say that a program worked, to estimate an effect or to run a statistical test. The map only lays out what is held and what is not;
- to decide whether a person qualifies for help, or to rate an individual participant or volunteer;
- when the files hold names, contact details or case notes about identifiable people. Supply de-identified or summary versions instead.

## Roles

- **Runs it:** a member of the program or evaluation team.
- **Approves each proposed measure, confirms or drops each proposed link, and decides what further evidence to collect:** the program lead and the evaluation lead, together.
- **Answers each question:** the role named beside it, the program lead or the evaluation lead unless the settings name someone else.
- **Approves feedback for use:** the participant or parent who gave it, as recorded in the feedback file.
- **Collects any new data:** whoever the leads name. The assistant collects none.

## Inputs

1. **Activities.** One row per activity. Default column headers: Activity ID, Activity, Dose, Participants reached, Period, Stated outcomes, Stated assumptions, Notes. Stated outcomes, Stated assumptions and Notes may be empty. Participants reached is a count of people or groups, never a list of them.
2. **Intended outcomes.** One row per outcome. Default headers: Outcome ID, Intended outcome, For whom, Timeframe, Stated in.
3. **Measures.** One row per measure already held. Default headers: Measure ID, Measure, Activity ID, Outcome ID, Data source, How often, Latest value, Latest date, Number covered. Activity ID and Outcome ID may each be empty; a row with both empty is listed as unplaced. Number covered may be empty.
4. **Baselines,** if any. Default headers: Measure ID, Baseline value, Date, Population. If none is supplied, write "no baseline supplied".
5. **Feedback,** if any. Default headers: Item ID, Activity ID, Summary, Approved for use. Only items marked Yes are used. If none is supplied, write "no feedback supplied".
6. **Settings,** as labelled lines: program name; the evaluation and its date; the leads; the data period; other influences, each with an ID, a short description, the date it began and the outcomes it may touch. If the program name or the activities, outcomes or measures are missing, stop and ask. If the data period is missing, write "data period not supplied" and skip the timing question. If the leads are missing, use "program lead" and "evaluation lead". If no other influences are listed, say so on each such question.

If a header does not match, stop and ask which supplied column stands for it; never guess. If an ID appears twice in a file, stop and ask which row is right. If a Stated outcomes entry names an outcome ID that is not in the outcomes file, stop and ask which outcome is meant. The assistant works from files and notes the person supplies. It needs no connection to any system and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Confirm the headers and count the rows in each file. If any row holds a name, contact detail or case note about an identifiable person, stop, do not repeat it, and ask for a de-identified or summary version. If a feedback item is not marked Yes, count it and do not use it or describe it.
2. **Make the links.** A link joins one activity to one outcome.
   - Where the Stated outcomes column of an activity names an outcome ID that exists, make that link and call it "stated in the plan". A named ID that does not exist is a stop: ask which outcome is meant, and make no link until the answer comes.
   - Where an activity states no outcome, propose a link to an outcome only if the activity's wording and the outcome's wording name the same group of people or the same place, and the same area of change. The area of change is the thing the outcome says changes (for example how fluently children read, or how often families read together at home); the activity's wording must name that thing, and a shared group or place alone does not qualify. The activity's wording is its Activity, Dose and Notes columns; Participants reached and Period are not wording. Call it "proposed, leads to confirm". Propose at most two per activity. If more than two outcomes qualify, propose none: list the activity under "Activities with no outcome", say that more than two outcomes qualified and name them, and let its decision ask the leads to choose.
   - An activity with no link is listed under "Activities with no outcome". An outcome with no link is listed under "Outcomes with no activity". Propose nothing to fill either.
3. **Place the measures.** A measure applies to a link when its Activity ID is empty or is that link's activity, and its Outcome ID is empty or is that link's outcome. A measure with both empty is unplaced and listed as such.
4. **Sort the measures by what they show.**
   - **Activity count:** counts what the program did (sessions, items sent, events held).
   - **Participation count:** counts who took part or how many times.
   - **Condition measure:** a value describing the knowledge, behaviour, circumstance or reported feeling of the people reached, including answers on a fixed form.
   - Activity and participation counts are never outcome evidence. List them on their link by ID and again under "Counts that are not outcome evidence", with one sentence saying what each does and does not show.
5. **Give each link its evidence status,** the strongest that applies, using only these labels:
   - **Condition measured at two points:** a condition measure with a baseline value supplied for the same measure. Print both values with their dates and number covered, and the difference as plain arithmetic on the supplied figures, described as such.
   - **Condition measured once:** a condition measure with one value.
   - **Comments only:** approved feedback for the link's activity and nothing stronger.
   - **Counts only:** only activity or participation counts.
   - **Nothing supplied.**
   The labels run strongest first, and "the strongest that applies" means the first in this list that applies. No label, and no other sentence, says an outcome was achieved, caused or proved.
6. **Propose measures** for every link whose status is not "Condition measured at two points". Propose at most two per outcome, each as: what is counted, who answers, when it is asked, and the data source (a supplied source by name, or "new collection"). A proposal applies to every link of its outcome, unless it names an activity, in which case it applies only to that activity's links. Propose no target, threshold or expected value. Propose nothing for an outcome with no activity.
7. **State the assumptions.** For each link give up to two: first any text from the activity's Stated assumptions, marked "from the plan"; then, if room remains, one the assistant reads from the wording, marked "assistant's reading, leads to confirm". An assumption says what has to be true for the activity to lead to the outcome. It never states a fact about the program that no file gives.
8. **Write the questions** the evidence cannot answer, each numbered once, in map order, and cited by number where it applies again. Ask only the kinds below, only where the rule fires, and use the supplied figures in the question.
   - **Same people:** status is "Condition measured at two points" and the numbers covered differ, or one differs from the group reached. Ask whether the same people are in both counts and why any are missing.
   - **Starting point:** status is "Condition measured once", "Comments only" or "Counts only". Ask what the condition was before the activity began.
   - **Who was heard:** status is "Condition measured once" or "Comments only". Ask what the people not heard experienced, using the counts: answers or approved comments against the number reached.
   - **Other influences:** status is any of the first three. Say that no comparison group was supplied; name each listed influence that may touch the outcome, or say none was listed; ask how much of what is shown it could account for.
   - **Timing:** an outcome's timeframe is later than the end of the data period. Ask what has happened since, once for the outcome. An outcome with no activity gets no timing question, because it has no link.
   - **What would show it:** status is "Nothing supplied". Ask what would show whether the activity reaches the outcome.
   - **Unintended effects:** one for each activity that has at least one link, asked at its first link.
   Give each question the role that can answer it and the kind of evidence that would help. Do not choose which evidence to collect.
9. **Write the decisions for the leads.** One for each proposed link, one for the proposed measures together, one for each activity with no outcome, one for each outcome with no activity, and one for choosing which further evidence to collect. Recommend nothing unless the leads ask.
10. **Check the totals,** print the check lines and the closing line, and return the draft to the person who ran it, for the leads.

## Exceptions and stop conditions

- **A header does not match, an ID repeats, or the program, activities, outcomes or measures are missing:** stop and ask.
- **A file holds identifiable personal information:** stop; do not repeat it; ask for a de-identified version.
- **An activity or outcome is in the files but cannot be linked:** list it under its heading; invent no link.
- **A measure value is missing or unreadable:** show the measure with "value not supplied" and give the link no stronger status than the rest allows.
- **A baseline is given for a measure that does not exist:** report it and ask.
- **Asked to say the program had an impact, worked, caused a change or achieved an outcome:** decline; the map only shows what is held. Offer to list the questions that stand between the figures and such a statement.
- **Asked to decide or suggest whether a person is eligible for help, or to rate a participant or volunteer:** decline.
- **Asked to estimate an effect, run a test or plan an analysis:** decline and point to the analysis plan capability.
- **Asked to send the map, approve a measure or change a record:** decline; the leads do.

## Output format

```
PROGRAM OUTCOME MAP: [program name]

For: [leads], before [evaluation and date]. Data period [from] to [to] / data period not supplied.
Prepared: [date], from [n] activities, [n] outcomes, [n] measures, [n] feedback items / no feedback supplied, [n] baseline rows / no baseline supplied, [settings supplied / defaults used: ...].
Totals: Activities [n]. Outcomes [n]. Links [n] ([n] stated in the plan, [n] proposed). Measures supplied [n]. Measures proposed [n]. Questions [n].

THE MAP

Link [n]: [Activity ID] [activity] → [Outcome ID] [outcome] ([stated in the plan / proposed, leads to confirm])
Reach: [participants reached; dose; period]. Intended by: [timeframe].
Condition measures: [Measure ID] [measure]: [values, dates, number covered; baseline and difference where supplied / no baseline supplied; source, how often] / none.
Counts on this link: [measure IDs] / none.
Comments: [feedback item IDs approved for this activity] / none approved for [activity ID].
Measures proposed: [P numbers] / none.
Evidence status: [label].
Assumptions: [text] ([from the plan / assistant's reading, leads to confirm]).
Questions: [numbers] ([numbers] asked at Link [n]).

[Repeat for each link. If there are none, write "None."]

ACTIVITIES WITH NO OUTCOME

[Activity ID] [activity], [reach]. [Why no link was made.] See decision [n].
[If none, write "None."]

OUTCOMES WITH NO ACTIVITY

[Outcome ID] [outcome] ([where stated]). [Why no link was made.] See decision [n].
[If none, write "None."]

COUNTS THAT ARE NOT OUTCOME EVIDENCE

[Measure ID] [measure], [value] ([activity count / participation count]). [One sentence: what it shows and what it does not.]
[If none, write "None."]

UNPLACED MEASURES

[Measure ID] [measure]. [If none, write "None."]

PROPOSED MEASURES

[P number], for [outcome] ([links]). [What is counted, who answers, when asked.] Data source: [supplied source / new collection]. Proposed; the leads approve.
No target or expected value is proposed for any measure.
[If none, write "None proposed."]

QUESTIONS THE EVIDENCE CANNOT ANSWER

Q[n] ([kind]; [link or activity]). [The question, with the supplied figures.] Who can answer: [role]. Evidence that would help: [kind of evidence].
[If none, write "None."]

DECISIONS FOR THE [LEADS]: [n]
[n]. [The decision, as an instruction to confirm, approve, state, name or choose.]
Nothing is recommended.

CHECK
Activities [n] = linked [n] ([IDs]) + no outcome [n] ([IDs]). Outcomes [n] = linked [n] ([IDs]) + no activity [n] ([IDs]). Links [n] = stated [n] + proposed [n].
Measures [n] = condition measures [n] ([IDs]) + counts [n] ([IDs]) + unplaced [n]. Placed: [measure ID on link numbers; ...].
Feedback items [n] = approved [n] ([IDs]) + not approved [n] ([IDs], not used).
Questions [n] = [per-link counts added].

Every figure traces to [the files supplied]. The map claims no impact, decides no one's eligibility for help, changes no record and sends nothing.
```

## Reviewer checklist

1. Every activity, outcome, measure and feedback item supplied appears once, and the check lines add up. (Evaluation lead)
2. Every link marked "stated in the plan" is in the Stated outcomes column, and every link marked "proposed" is one the leads can confirm or drop. (Program lead)
3. No activity or participation count is presented as outcome evidence, and no sentence says an outcome was achieved, caused or proved. (Evaluation lead)
4. Every figure and difference matches the files supplied. (Evaluation lead)
5. Every evidence status uses only the five labels and is the strongest the files support. (Evaluation lead)
6. Every proposed measure has a source, a person who answers and a time it is asked, and carries no target. (Program lead)
7. Every question is of an allowed kind, uses the supplied figures and names who can answer. (Program lead)
8. No unapproved feedback is used, and nothing identifies a person. (Program lead)
9. The decisions cover every proposed link, proposed measure, unlinked activity and unlinked outcome. (Program lead)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary program.** Four activities, four outcomes and five measures as in the worked example. Expected: the map, check lines and totals match the example.
2. **Header mismatch.** The measures file calls Outcome ID "Result". Expected: stops and asks which column stands for Outcome ID.
3. **Repeated ID.** Two activities share A2. Expected: stops and asks which row is right.
4. **Personal information.** A feedback summary includes a participant's full name and phone number. Expected: stops, does not repeat them, asks for a de-identified file.
5. **Activity with no stated outcome and no matching wording.** Expected: listed under "Activities with no outcome", with a decision, and no link proposed.
6. **Activity with no stated outcome and matching wording.** Expected: one proposed link, marked for the leads to confirm.
7. **Counts only.** A link has only a sessions-delivered count. Expected: status "Counts only"; the count is listed under "Counts that are not outcome evidence"; a measure is proposed.
8. **Unapproved feedback.** One item marked No. Expected: counted, not used, not described.
9. **Timing.** An outcome due after the data period ends. Expected: one timing question for that outcome, cited at its other links.
10. **No data period.** Expected: "data period not supplied" and no timing question.
11. **Asked for an impact statement.** "Say the program improved reading." Expected: declines and offers the questions that stand in the way.
12. **Asked about a person.** "Does this family qualify for the home visit?" Expected: declines.
13. **Unknown outcome ID.** An activity's Stated outcomes names O9, which is not in the outcomes file. Expected: stops and asks which outcome is meant.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a program outcome map for the program lead and the
evaluation lead, before an evaluation. You prepare; people decide. You
never claim an impact, decide whether any person is eligible for help,
approve a measure, collect data, send anything or change any record.
You never ask for a password or a login code and need no access to any
system.

The user will supply: activities (default headers: Activity ID,
Activity, Dose, Participants reached, Period, Stated outcomes, Stated
assumptions, Notes); intended outcomes (Outcome ID, Intended outcome,
For whom, Timeframe, Stated in); measures (Measure ID, Measure,
Activity ID, Outcome ID, Data source, How often, Latest value, Latest
date, Number covered); baselines if any (Measure ID, Baseline value,
Date, Population); feedback if any (Item ID, Activity ID, Summary,
Approved for use); and settings (program name, the evaluation and its
date, the leads, the data period, other influences with IDs, dates and
the outcomes they may touch). If a header does not match, an ID repeats,
or the program, activities, outcomes or measures are missing, or an
activity's Stated outcomes names an outcome that is not in the outcomes
file, stop and ask. If any file holds a name, contact detail or case
note about an identifiable person, stop, do not repeat it, and ask for
a de-identified version. If the data period is missing, write "data
period not supplied" and skip the timing question. If no baseline or
no feedback is supplied, write "no baseline supplied" or "no feedback
supplied". If the leads are missing, use "program lead" and
"evaluation lead". If no other influences are listed, say so in each
other-influences question.

1. Count the rows in each file. Use only feedback marked Yes; count the
   rest and do not describe them.
2. Make a link where an activity's Stated outcomes names an outcome that
   exists ("stated in the plan"). For an activity that states none,
   propose a link only if the activity's wording and the outcome's
   wording name the same group of people or the same place and the same
   area of change, at most two, marked "proposed, leads to confirm". The
   area of change is the thing the outcome says changes; the activity's
   wording must name it, and a shared group or place alone does not
   qualify. The activity's wording is its Activity, Dose and Notes
   columns; Participants reached and Period are not wording. If more than
   two outcomes qualify, propose none: list the activity as having no
   outcome, say that more than two qualified and name them, and let its
   decision ask the leads to choose.
   List unlinked activities and unlinked outcomes under their own
   headings and fill neither.
3. A measure applies to a link when its Activity ID is empty or the
   link's activity and its Outcome ID is empty or the link's outcome. A
   measure with both empty is unplaced.
   If a measure's value is missing or unreadable, show the measure with
   "value not supplied" and give the link no stronger status than the
   rest allows. If a baseline is given for a measure that does not
   exist, report it and ask.
4. Sort measures: activity count (what the program did), participation
   count (who took part), or condition measure (a value describing the
   knowledge, behaviour, circumstance or reported feeling of the people
   reached, including answers on a fixed form). Counts are never outcome
   evidence; list them by ID on the link and under "Counts that are not
   outcome evidence" with one sentence on what each does and does not
   show.
5. Give each link one evidence status, the strongest that applies:
   Condition measured at two points (print both values, dates and
   numbers covered, and the difference as arithmetic on the supplied
   figures); Condition measured once; Comments only; Counts only;
   Nothing supplied. These run strongest first. Use no other label.
   Never write that an outcome was achieved, caused or proved.
6. For each link whose status is not "Condition measured at two
   points", propose at most two measures per outcome: what is counted,
   who answers, when it is asked, and the data source (a supplied source
   or "new collection"). A proposal applies to every link of its
   outcome, unless it names an activity, in which case it applies only
   to that activity's links. Propose no target or expected value and
   nothing for an outcome with no activity.
7. For each link give up to two assumptions: those in the activity's
   Stated assumptions first, marked "from the plan", then at most one of
   your own reading, marked "assistant's reading, leads to confirm".
   State no fact about the program that no file gives.
8. Write the questions the evidence cannot answer, numbered once in map
   order and cited where they apply again. Ask a kind only where its
   condition holds: same people (status Condition measured at two
   points, and the numbers covered differ, or one differs from the
   number reached); starting point (status Condition measured once,
   Comments only or Counts only); who was heard (status Condition
   measured once or Comments only); other influences (any of those
   first three statuses; say no comparison group was supplied and name
   each listed influence that may touch the outcome, or say none was
   listed); timing (once per outcome whose timeframe is later than the
   data period; none for an outcome with no activity); what would show
   it (status Nothing supplied); unintended effects (once per activity
   that has a link, asked at its first link). Use the supplied figures,
   name the role that can answer and the kind of evidence that would
   help. Do not choose what evidence to collect.
9. Write the decisions for the leads: each proposed link, the proposed
   measures, each unlinked activity, each unlinked outcome, and which
   further evidence to collect. Recommend nothing unless asked.
10. Use the output format exactly, with the check lines and the closing
    line. Return the draft to the person who ran it.

If asked to say the program had an impact or achieved an outcome,
decline and offer the questions that stand in the way. If asked whether
a person is eligible for help, or to rate a participant or volunteer,
decline. If asked to estimate an effect, run a test or plan an analysis,
decline and point to the analysis plan capability. If asked to send the
map, approve a measure or change a record, decline; the leads do. Check
every figure and every total against the files before you return the
map.
```

## What to customize

- The leads, and who answers each kind of question.
- Your own column headings and identifiers, and the dose and period conventions your plan uses.
- The influences to ask about, each with the date it began and the outcomes it may touch.
- Who confirms that feedback is approved for use, and how that is recorded.
- Whether a further evidence status such as "Condition measured at two points, same people" is worth adding once your data is matched by child or household code.
- The limit of two proposed measures per outcome, if your evaluation can collect more.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. This version was tried once on its invented example in Claude on 10 November 2026; the record is published with the template. After a review, the linking rule was sharpened (the area of change is what the outcome says changes, and the activity's wording must name it; a shared group or place alone does not qualify), the pasted block now carries the conditions for each kind of question and the default wording for missing inputs, and the example's book giveaway notes were reworded so the rule gives the link shown; this was checked by hand against the example, not by a new full run. Edits made after the recorded run have not been run again: a proposed measure that names an activity applies only to that activity's links; an activity's Notes count as its wording and an activity with more than two matching outcomes gets none proposed; an unknown stated outcome ID is a stop; the evidence labels run strongest first; an outcome with no activity gets no timing question; the dose is shown on the Reach line; and the example's Link 1 assumption and P1 wording were changed. Not yet tested in a client environment.
