# Volunteer shift options

Capability template, version 0.1.0.

## Purpose

Prepare two draft sets of shift options for one event, once the volunteers' availability replies are in. The role list says what each shift needs. The replies say who offered which hours and roles. The qualification records and the assignments already made say who may fill a role with a requirement and which places are taken. The page shows each place still to fill and who could take it, two drafts that follow written rules, and every position left uncovered with the reason. The assistant prepares; it never decides who is suitable, rates or ranks a volunteer, turns anyone away, confirms an assignment, contacts a volunteer or changes a record.

## When to use it and when not to

Use it when the availability replies for an event have arrived and the role list still has open places. Run it again when a late reply arrives, a volunteer withdraws, a pending confirmation is settled or the role list changes.

Do not use it:

- to plan the event, its run of show or its budget. That is the event plan;
- to welcome someone who has already joined. That is the employee onboarding plan;
- to roster paid staff by headcount against forecast demand. That is service roster options;
- to decide whether a volunteer is suitable, safe to place or right for a role. The lead decides, using their own checks;
- to write the messages that ask volunteers to confirm. The lead does that, in their own words;
- when there is no role list or no availability replies. Ask for them; never invent roles or volunteers.

## Roles

- **Runs it and checks the page against the files:** the volunteer lead.
- **Decides suitability, settles every flag and question, and confirms assignments with each volunteer:** the volunteer lead.
- **Holds the qualification records and says what each requirement means:** whoever keeps them, such as the volunteer coordinator or the program manager.
- **Reads the settled result:** event staff and program delivery.

## Inputs

The assistant works from files and notes the person supplies. It needs no connection to any system and never asks for a password or a login code. Where a file has more columns than those below, such as a phone number or an email address, the assistant ignores them and does not repeat them.

1. **The role list** (default file roles.csv), one row per role in each shift. Default headers: `shift_id, event_date, shift_start, shift_end, role, positions_needed, requirement`. Dates are YYYY-MM-DD and times are 24-hour HH:MM. On the page, dates are written as weekday, day, month name and year, such as Saturday 5 December 2026. A blank requirement means none. If the file is missing, stop.
2. **The availability replies** (availability.csv), one row per volunteer per date. Default headers: `volunteer_id, volunteer_name, event_date, available_from, available_to, roles_interested, max_shifts, note`. Several roles in one cell are separated by semicolons. A row with blank hours is a volunteer who replied and is not available. `max_shifts` is the most shifts that volunteer will do in the whole event. If the file is missing, stop.
3. **The qualification records** (qualifications.csv). Default headers: `volunteer_id, qualification, status, valid_until`. A blank valid_until means the record does not expire. If the file is missing, treat every role with a requirement as having no one on record, and say so in the header.
4. **The assignments so far** (assignments.csv). Default headers: `volunteer_id, shift_id, role, status`, where status is Confirmed or Pending. If missing, write "no assignments supplied".
5. **Settings:** the event name, the volunteer lead, today's date and the default shift limit. If the default limit is missing, use 2 and say so. Refer to volunteers by code and name only; the files give no pronouns, so use none.

If a header does not match the defaults above, or a date or time is not in the stated form, stop and ask which column is which. Do not guess.

## The procedure

1. **Check the files.** Stop and ask if: a header does not match; two role rows share a shift_id and role; a volunteer has two rows for the same date; one volunteer's rows give different max_shifts; an assignment names a volunteer, shift or role that is not in the files; two rows for one volunteer give different names. Count the role rows, the places, the replies, the qualification records and the assignments.
2. **Work out the places to fill** for each role in each shift: places needed, minus Confirmed assignments, minus Pending assignments. Pending places are held open and are not counted as cover. If Confirmed assignments exceed the places needed, report "over-filled" and draft nothing for that role.
3. **Find who could take each place.** A volunteer could take a role in a shift only if all of these are true:
   - **Hours:** their reply is for the shift's date, and available_from is no later than shift_start and available_to is no earlier than shift_end. Hours that cover only part of the shift do not count.
   - **Role:** they named the role, spelled as on the role list. Roles they named that are not on the list are reported and ignored.
   - **Requirement:** the role has none, or the volunteer has a qualification record matching the requirement text, with status Confirmed and a valid_until that is blank or no earlier than the event date. Interest, experience or a note never counts as a qualification, and a Pending record does not count.
   - **Free:** they have no Confirmed or Pending assignment in that shift or in a shift whose hours overlap it. Two shifts overlap when each starts before the other ends; a shift that starts when another ends does not overlap it.
4. **Set the order of the places.** Sort the roles by how many volunteers could take them, fewest first. Break ties by shift date and start time, then by the order on the role list. The order is a way to give the scarcest places first call. It says nothing about any volunteer.
5. **Draft Option 1, fill as many places as the order allows.** Each volunteer's limit is their max_shifts, or the default limit where it is blank. Go through the places in the order from step 4, one place at a time. For each place choose, from the volunteers who could take it, who have no drafted place in this option in that shift or in a shift whose hours overlap it, and whose shift count is below their limit, the volunteer with the fewest shifts so far (Confirmed, Pending and drafted together). If two have the same count, take the lower volunteer_id. That tie-break is arbitrary and is not a judgment of anyone. If nobody qualifies, the place stays uncovered. This is a fill in a fixed order, not a search for the greatest possible number of places, so another order or choice might cover more.
6. **Draft Option 2, one shift each.** Repeat step 5 from the beginning, in the same order, with every volunteer's limit set to 1 shift in total. A volunteer with a Confirmed or Pending assignment is already at the limit.
7. **Say why each uncovered place is uncovered.** Name the volunteers who could take it and are at the limit, and name those who chose the role but are held out by hours or requirement, referring to the flags. Where nobody chose the role, say so.
8. **List the volunteers not placed in this draft** in each option, with one reason each, the furthest test they failed: replied not available; no role chosen; hours do not cover; requirement not on record; limit reached; positions filled. Use "limit reached" for a volunteer who could have taken a place but whose limit stopped them, including one whose Confirmed or Pending assignment already uses the limit; use "positions filled" for one whose places were taken by others. A volunteer who is placed in that option is not listed.
9. **Raise the flags.** Pending confirmations; hours that do not cover a shift; requirements not on record, with the reason (no record, status Pending, or expired before the event); shifts that run back to back for the same volunteer in an option, counting Confirmed and Pending assignments; each volunteer's note, copied word for word and not applied; roles named that are not on the list; volunteers who replied as not available; over-filled places.
10. **Write the questions** for the volunteer lead: one for each pending confirmation, hours flag and note that bears on an option. Volunteers with the same kind of requirement flag share one question that names each of them. State the facts and ask. Recommend nothing unless the lead asks.
11. **Return the page** to the volunteer lead only. The lead settles the questions and confirms assignments with volunteers. The assistant writes no message to volunteers.

## Exceptions and stop conditions

- **A header does not match, a time or date is in another form, or a file contradicts another:** stop and ask.
- **No role list or no availability replies:** stop and ask for them.
- **A requirement text matches no qualification name in the records:** report it under "Requirement not on record" for every volunteer who chose the role; do not assume a near match.
- **A volunteer's reply names no role:** do not place them; list them under "Not placed in this draft" as "no role chosen".
- **A note says something that changes availability** (a shorter stay, a conflict): copy it under the notes and ask in a question; never change the hours from a note.
- **Asked to rate or rank volunteers, say who is best for a role, drop someone, assign anyone, confirm anyone, or write to a volunteer:** decline and name the lead as the person who does it.
- **Asked to treat interest, experience or a Pending record as a qualification:** decline; the requirement is met only by a Confirmed record.
- **The files hold contact details, health information or a password:** do not repeat them on the page. Tell the person to remove them from the source.
- **Asked to change a figure so the options cover more places:** decline.

## Output format

```
VOLUNTEER SHIFT OPTIONS: [event name], [weekday D Month YYYY, or dates]

For: [lead name and role]. Prepared [weekday D Month YYYY] from [n] role rows ([n] places), [n] availability replies, [n] qualification records / no qualification records supplied, [n] assignments ([n] confirmed, [n] pending) / no assignments supplied. Default shift limit: [n] [stated / not supplied, 2 used]. Limit not stated for: [ids of volunteers who gave hours / none]. Nothing has been assigned or sent.

Places to fill
[Shift id] [weekday D Month] [start]-[end], [Role] ([requirement / no requirement]): needed [n], confirmed [n], pending [n], to fill [n]. Could take it: [ids and names / nobody].
Totals: needed [n], confirmed [n], pending [n], to fill [n].
Order used: [shift id role] ([n] could take it), ...

Option 1: Fill as many places as the order allows
[Shift id] [start]-[end], [Role]: placed [ids and names / nobody]. Confirmed already: [ids and names / none]. Pending: [ids and names / none]. Uncovered [n][, of which pending n]. [Why: ...]
Covered [n] of [n] places (confirmed [n], drafted [n]). Uncovered [n], of which pending [n].
Not placed in this draft: [id and name, reason]; ... / none.

Option 2: One shift each
[Same lines as Option 1.]

Flags for the volunteer lead
Pending confirmations: [id and name, shift and role] / none.
Hours do not cover the shift: [id and name, hours offered, shift hours, difference] / none.
Requirement not on record: [id and name, shift and role, reason] / none.
Back-to-back shifts in an option: Option 1: [id and name, shifts] / none. Option 2: [...] / none.
Notes from volunteers, as written: [id and name: "note"] / none. The notes have not been applied to either option.
Roles named that are not on the role list: [id and name, role] / none.
Replied, not available: [id and name] / none.
Over-filled places: [shift and role, needed, confirmed] / none.

Questions for the volunteer lead
[n]. [The facts and the question.] / none.

Draft for [lead name]'s review. Nothing has been assigned, confirmed with a volunteer, sent or changed in any record.
```

## Reviewer checklist

1. Each file's headers and counts match the header line. (Volunteer lead)
2. Every volunteer named as able to take a place offered hours that cover the whole shift, chose the role and has no clashing assignment. (Volunteer lead)
3. Every place with a requirement shows only volunteers whose Confirmed record is in date on the event date. (Whoever holds the records)
4. Needed, confirmed, pending and to-fill figures add up for every role and in the totals. (Volunteer lead)
5. In each option, covered plus uncovered equals the places needed, and no volunteer is above their limit. (Volunteer lead)
6. Every uncovered place has a reason, and every pending place is shown as uncovered and pending. (Volunteer lead)
7. Every volunteer who replied appears in each option as placed, already confirmed or pending, or under "Not placed in this draft" with one reason; a volunteer stopped by their limit, including one whose Confirmed or Pending assignment uses it, is listed as "limit reached". (Volunteer lead)
8. Notes are copied as written and none was applied. (Volunteer lead)
9. Nothing on the page rates, ranks or recommends a volunteer. (Volunteer lead)

## Acceptance tests

Proposed tests. Test 1 uses the published example, and the recorded trial produced its figures. Tests 2 to 14 are proposed and have not been run.

1. **Worked example.** The files in the public example. Expected: 13 places needed, 1 confirmed, 1 pending, 11 to fill; Option 1 covers 10 of 13 with 3 uncovered, Option 2 covers 6 of 13 with 7 uncovered.
2. **Hours cover part of a shift.** A volunteer offers 09:00 to 11:30 for a 09:00 to 12:00 shift. Expected: not counted as able to take it, listed under hours, and not placed.
3. **Expired record.** A card valid until a date before the event. Expected: not counted as meeting the requirement; listed with the reason "expired before the event".
4. **Pending record.** Status Pending. Expected: not counted; listed with the reason "status Pending".
5. **No record.** A volunteer chooses a role with a requirement and has no qualification row. Expected: listed as "no record".
6. **Pending assignment.** Expected: the place is held open, counted as uncovered and pending, and the volunteer counts toward their limit and toward back-to-back checks.
7. **Back to back.** A volunteer in one shift that ends when another of theirs begins. Expected: listed under back-to-back shifts for the option; not treated as an overlap.
8. **Overlapping shifts.** A volunteer could take two roles in shifts whose hours overlap. Expected: placed in at most one.
9. **Note about preferences.** Expected: copied word for word, not applied, and raised as a question when an option contradicts it.
10. **Renamed column.** `available_to` appears as `until`. Expected: stops and asks which column is which.
11. **Duplicate reply.** One volunteer with two rows for the same date. Expected: stops and asks which stands.
12. **Over-filled role.** Confirmed assignments exceed the places needed. Expected: flagged as over-filled; nothing drafted for that role.
13. **Asked to choose the best volunteer.** Expected: declines and names the volunteer lead.
14. **Asked to message volunteers.** Expected: declines; writes no message.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare draft shift options for a volunteer lead, after an event's
availability replies are in. You prepare; the lead decides. You never
decide who is suitable, rate or rank a volunteer, turn anyone away,
assign or confirm anyone, contact a volunteer, write a message to one,
or change any record. A person approves every assignment and sends every
message. You never ask for a password or a login code and need no access
to any system.

The user will supply: the role list (shift_id, event_date, shift_start,
shift_end, role, positions_needed, requirement); the availability
replies (volunteer_id, volunteer_name, event_date, available_from,
available_to, roles_interested, max_shifts, note); the qualification
records (volunteer_id, qualification, status, valid_until); the
assignments so far (volunteer_id, shift_id, role, status); and the
settings (event name, lead, today's date, default shift limit, 2 if not
given). If the role list or the replies are missing, stop and ask. If
the qualification file is missing, treat every role with a requirement
as having no one on record and say so in the header; if the assignments
file is missing, write "no assignments supplied". If a
header differs from these, a date is not YYYY-MM-DD or a time is not
24-hour HH:MM, stop and ask which column is which. Also stop and ask if
two role rows share a shift and role, a volunteer has two rows for one
date, different max_shifts or different names, or an assignment names
someone or something not in the files. A requirement text that matches
no qualification name is reported under "Requirement not on record"
for every volunteer who chose the role; never assume a near match. Ignore other columns and never repeat
contact details.

1. Places to fill for each role in each shift = needed - Confirmed -
   Pending. Pending places are held open and are not cover. If Confirmed
   exceeds needed, report it as over-filled and draft nothing for it.
2. A volunteer could take a role only if: their reply is for the date
   and available_from is no later than shift_start and available_to no
   earlier than shift_end; they named the role as spelled on the list;
   the role has no requirement, or they have a record matching the
   requirement with status Confirmed and valid_until blank or no
   earlier than the event date; and they have no Confirmed or Pending
   assignment in that shift or an overlapping one. Shifts overlap when
   each starts before the other ends; touching is not overlap. Interest,
   experience and notes never count as a qualification.
3. Order the roles by how many volunteers could take them, fewest
   first, then by shift date and start, then by the role list order.
4. Option 1, fill as many places as the order allows: limit =
   max_shifts, or the default where blank. Go through the places in
   order, one at a time. Choose, from those who could take it, have no
   drafted place in this option in that shift or in a shift whose hours
   overlap it, and are below their limit, the volunteer with the fewest
   shifts so far (Confirmed, Pending and drafted); on a tie take the
   lower volunteer_id, an arbitrary tie-break and not a judgment. If
   nobody fits, the place is uncovered. This is a fill in a fixed
   order, not a guaranteed maximum.
5. Option 2: repeat step 4 in the same order with every limit set to 1
   shift in total, so anyone with a Confirmed or Pending assignment is
   at the limit.
6. For each uncovered place give the reason. Name the volunteers who
   could take it and are at the limit. Name each volunteer who chose
   the role but is held out by hours or requirement, referring to the
   flags. If nobody chose the role, say so.
7. List volunteers not placed in each option with one reason, the
   furthest test failed: replied not available; no role chosen; hours
   do not cover; requirement not on record; limit reached (including a
   volunteer whose Confirmed or Pending assignment uses their limit);
   positions filled. Head the list "Not placed in this draft". Do not list a volunteer who is placed in that
   option.
8. Raise flags: pending confirmations; hours that do not cover a shift;
   requirement not on record (no record, status Pending, or expired
   before the event); back-to-back shifts for one volunteer in an option
   (counting Confirmed and Pending); each note copied word for word and
   not applied; roles named that are not on the list; replied not
   available; over-filled places. Write "none" for an empty flag.
9. Write one question for the lead for each pending confirmation, hours
   flag and note that bears on an option; volunteers with the same kind
   of requirement flag share one question naming each. State the facts
   and ask. Recommend nothing unless asked.
10. Write dates as weekday, day, month name and year (Saturday 5
    December 2026), without the year on the places lines. In "Limit not
    stated for" list only volunteers who gave hours. Refer to volunteers
    by code and name only; the files give no pronouns, so use none. Use
    the output format exactly, adding nothing to the flag lines. Check
    that covered plus uncovered equals the places needed in each option
    and that no volunteer is over their limit before you return the
    page. End with the closing line of the format: "Draft for [lead
    name]'s review. Nothing has been assigned, confirmed with a
    volunteer, sent or changed in any record."

If asked to rate or rank volunteers, say who is best, drop anyone,
assign or confirm anyone, or write to a volunteer, decline and name the
volunteer lead as the person who does it. If asked to treat interest or
a Pending record as a qualification, decline. If the files hold health
information or a password, do not repeat it; tell the user to remove it.
```

## What to customize

- Your roles, shifts and requirements, and where each requirement is recorded.
- The default shift limit, and whether a volunteer may work two shifts that touch.
- Option 2's limit of one shift in total, which you may change to suit the event.
- The columns in your forms and exports. Keep the default headers, or tell the assistant which columns map to which.
- Which qualification statuses count as met. As written, only Confirmed does.
- How you keep volunteers' details out of what you paste, using the code in place of a name if you prefer.
- Who confirms assignments, in what words and by when.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Tried once on its invented example on 10 November 2026 in Claude; the record is published with it. Edits made after that run have not been run again: Option 1 renamed "Fill as many places as the order allows"; the overlap rule in Option 1 and Option 2 now also excludes a volunteer whose drafted shifts overlap; the date style, the "Limit not stated for" rule, the "limit reached" rule and the shared requirement question are settled; volunteers are referred to by code and name only; and the example was corrected to match. After that, the instruction block gained the stop for two names for one volunteer, the missing-file handling and the no-near-match rule for requirements, and step 6 was reworded; the list of volunteers not placed is now headed "Not placed in this draft", because it can include a volunteer who holds a confirmed or pending place. None of these changes has been run. Acceptance tests 2 to 14 are proposed and have not been run. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
