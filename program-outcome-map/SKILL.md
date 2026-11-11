---
name: "program-outcome-map"
description: "Prepare, before an evaluation, one map that links each activity of a program to the outcome it is meant to serve, from the program's own plan, measures and approved feedback. For each link the map shows the measures already held, the measures worth proposing, where the data comes from, the assumption that has to hold, what the evidence behind the link actually is, and the numbered questions that evidence cannot answer. The assistant prepares; it never claims an impact, never decides whether any person is eligible for help, never approves a measure, never collects data and never changes a record."
license: "MIT"
metadata:
  version: "0.1.0"
  publisher: "Fully Powered AI"
  capability: "Program outcome map"
---

# Program outcome map

This is the technical file for a Fully Powered capability template. It carries the instructions an AI product follows. The complete template, with roles, inputs, exceptions, the reviewer checklist, acceptance tests and what to customize, is in [TEMPLATE.md](TEMPLATE.md). A worked example with invented data is in [EXAMPLE.md](EXAMPLE.md).

## Instructions

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

## Before relying on it

Decide every item under "What to customize" in TEMPLATE.md and set the limits the instructions in this file leave open, written in square brackets such as [N], to your own. Then run the acceptance tests in TEMPLATE.md on past work. A person starts this work, supplies the inputs and decides what happens with the result.
