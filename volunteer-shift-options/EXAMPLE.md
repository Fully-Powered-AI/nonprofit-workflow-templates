# Volunteer shift options: an invented example

*Illustrative example with invented data.* Marrow Creek Community Meals is an invented nonprofit, and the event, the volunteers, the codes, the cards and every figure below are invented. The volunteers are written as a code and a first name with an initial. First come the inputs the volunteer lead supplied, in full, then the page the capability returned.

## The inputs

```
SETTINGS
Event: Autumn Neighbor Supper
Volunteer lead: Noor Hale
Today: Tuesday 10 November 2026
Default shift limit per volunteer: 2

ROLE LIST (roles.csv)
shift_id,event_date,shift_start,shift_end,role,positions_needed,requirement
S1,2026-12-05,09:00,12:00,Setup crew,3,
S1,2026-12-05,09:00,12:00,Kitchen helper,2,Food handler card
S2,2026-12-05,12:00,15:00,Serving line,3,Food handler card
S2,2026-12-05,12:00,15:00,Greeter,2,
S3,2026-12-05,15:00,17:00,Cleanup crew,3,

AVAILABILITY REPLIES (availability.csv)
volunteer_id,volunteer_name,event_date,available_from,available_to,roles_interested,max_shifts,note
V01,Alma R.,2026-12-05,09:00,17:00,Setup crew;Cleanup crew,2,
V02,Bruno T.,2026-12-05,09:00,12:00,Setup crew;Kitchen helper,1,
V03,Cleo M.,2026-12-05,09:00,15:00,Kitchen helper;Serving line,2,
V04,Dev K.,2026-12-05,12:00,17:00,Greeter;Serving line;Cleanup crew,2,
V05,Esme L.,2026-12-05,09:00,11:30,Setup crew,,Can only stay until 11:30
V06,Farid N.,2026-12-05,12:00,17:00,Serving line,1,
V07,Greta P.,2026-12-05,09:00,17:00,Setup crew;Greeter;Cleanup crew,3,Prefers not to work two shifts back to back
V08,Hugo S.,2026-12-05,12:00,17:00,Greeter;Cleanup crew,2,
V09,Ivy D.,2026-12-05,09:00,15:00,Serving line;Kitchen helper,2,
V10,Jonas B.,2026-12-05,15:00,17:00,Cleanup crew,1,
V11,Kira O.,2026-12-05,,,,,Away that weekend

QUALIFICATION RECORDS (qualifications.csv)
volunteer_id,qualification,status,valid_until
V03,Food handler card,Confirmed,2027-03-31
V04,Food handler card,Confirmed,2027-06-30
V06,Food handler card,Confirmed,2026-11-30
V09,Food handler card,Pending,

ASSIGNMENTS SO FAR (assignments.csv)
volunteer_id,shift_id,role,status
V07,S2,Greeter,Confirmed
V08,S3,Cleanup crew,Pending
```

## The output

```
VOLUNTEER SHIFT OPTIONS: Autumn Neighbor Supper, Saturday 5 December 2026

For: Noor Hale, volunteer lead. Prepared Tuesday 10 November 2026 from 5 role rows (13 places), 11 availability replies, 4 qualification records, 2 assignments (1 confirmed, 1 pending). Default shift limit: 2 stated. Limit not stated for: V05. Nothing has been assigned or sent.

Places to fill
S1 Saturday 5 December 09:00-12:00, Setup crew (no requirement): needed 3, confirmed 0, pending 0, to fill 3. Could take it: V01 Alma R., V02 Bruno T., V07 Greta P.
S1 Saturday 5 December 09:00-12:00, Kitchen helper (Food handler card): needed 2, confirmed 0, pending 0, to fill 2. Could take it: V03 Cleo M.
S2 Saturday 5 December 12:00-15:00, Serving line (Food handler card): needed 3, confirmed 0, pending 0, to fill 3. Could take it: V03 Cleo M., V04 Dev K.
S2 Saturday 5 December 12:00-15:00, Greeter (no requirement): needed 2, confirmed 1, pending 0, to fill 1. Could take it: V04 Dev K., V08 Hugo S.
S3 Saturday 5 December 15:00-17:00, Cleanup crew (no requirement): needed 3, confirmed 0, pending 1, to fill 2. Could take it: V01 Alma R., V04 Dev K., V07 Greta P., V10 Jonas B.
Totals: needed 13, confirmed 1, pending 1, to fill 11.
Order used: S1 Kitchen helper (1 could take it), S2 Serving line (2), S2 Greeter (2), S1 Setup crew (3), S3 Cleanup crew (4).

Option 1: Fill as many places as the order allows
S1 09:00-12:00, Setup crew: placed V01 Alma R., V02 Bruno T., V07 Greta P. Confirmed already: none. Pending: none. Uncovered 0.
S1 09:00-12:00, Kitchen helper: placed V03 Cleo M. Confirmed already: none. Pending: none. Uncovered 1. Why: V03 is the only volunteer who chose it and could take it, and V03 already holds the one place drafted here; V02 and V09 are under "Requirement not on record".
S2 12:00-15:00, Serving line: placed V04 Dev K., V03 Cleo M. Confirmed already: none. Pending: none. Uncovered 1. Why: V06 and V09 are under "Requirement not on record".
S2 12:00-15:00, Greeter: placed V08 Hugo S. Confirmed already: V07 Greta P. Pending: none. Uncovered 0.
S3 15:00-17:00, Cleanup crew: placed V10 Jonas B., V01 Alma R. Confirmed already: none. Pending: V08 Hugo S. Uncovered 1, of which pending 1. Why: the last place is held for V08's pending confirmation.
Covered 10 of 13 places (confirmed 1, drafted 9). Uncovered 3, of which pending 1.
Not placed in this draft: V05 Esme L., hours do not cover; V06 Farid N., requirement not on record; V09 Ivy D., requirement not on record; V11 Kira O., replied not available.

Option 2: One shift each
S1 09:00-12:00, Setup crew: placed V01 Alma R., V02 Bruno T. Confirmed already: none. Pending: none. Uncovered 1. Why: V07 could take it but is at the limit (confirmed for S2 Greeter); V05 chose it but the hours do not cover the shift.
S1 09:00-12:00, Kitchen helper: placed V03 Cleo M. Confirmed already: none. Pending: none. Uncovered 1. Why: V03 is the only volunteer who chose it and could take it, and V03 already holds the one place drafted here; V02 and V09 are under "Requirement not on record".
S2 12:00-15:00, Serving line: placed V04 Dev K. Confirmed already: none. Pending: none. Uncovered 2. Why: V03 is at the limit; V06 and V09 are under "Requirement not on record".
S2 12:00-15:00, Greeter: placed nobody. Confirmed already: V07 Greta P. Pending: none. Uncovered 1. Why: V04 is at the limit; V08 is at the limit (pending for S3).
S3 15:00-17:00, Cleanup crew: placed V10 Jonas B. Confirmed already: none. Pending: V08 Hugo S. Uncovered 2, of which pending 1. Why: V01, V04 and V07 are at the limit; one place is held for V08's pending confirmation.
Covered 6 of 13 places (confirmed 1, drafted 5). Uncovered 7, of which pending 1.
Not placed in this draft: V05 Esme L., hours do not cover; V06 Farid N., requirement not on record; V07 Greta P., limit reached; V08 Hugo S., limit reached; V09 Ivy D., requirement not on record; V11 Kira O., replied not available.

Flags for the volunteer lead
Pending confirmations: V08 Hugo S., S3 Cleanup crew.
Hours do not cover the shift: V05 Esme L. offered 09:00-11:30; S1 Setup crew runs 09:00-12:00, 30 minutes longer.
Requirement not on record: V02 Bruno T., S1 Kitchen helper needs a Food handler card and no record exists. V06 Farid N., S2 Serving line: card Confirmed but valid until 2026-11-30, before the event. V09 Ivy D., S1 Kitchen helper and S2 Serving line: card status Pending.
Back-to-back shifts in an option: Option 1: V03 Cleo M., S1 Kitchen helper then S2 Serving line. V07 Greta P., S1 Setup crew then V07's confirmed S2 Greeter. V08 Hugo S., S2 Greeter then V08's pending S3 Cleanup crew. Option 2: none.
Notes from volunteers, as written: V05 Esme L.: "Can only stay until 11:30". V07 Greta P.: "Prefers not to work two shifts back to back". V11 Kira O.: "Away that weekend". The notes have not been applied to either option.
Roles named that are not on the role list: none.
Replied, not available: V11 Kira O.
Over-filled places: none.

Questions for the volunteer lead
1. V08 Hugo S. is pending for S3 Cleanup crew. Is that confirmed or released? Option 1 also places V08 in S2 Greeter, the shift before it.
2. V07 Greta P. wrote "Prefers not to work two shifts back to back". Option 1 places V07 in S1 Setup crew, which ends when V07's confirmed S2 Greeter shift begins. Is that acceptable to V07, and to you?
3. V05 Esme L. can stay only until 11:30. Is a shorter stay acceptable for S1 Setup crew?
4. V02, V06 and V09 have no usable Food handler card on record. Can any record be confirmed before 5 December? S1 Kitchen helper and S2 Serving line each have one place uncovered in Option 1.

Draft for Noor Hale's review. Nothing has been assigned, confirmed with a volunteer, sent or changed in any record.
```
