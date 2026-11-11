# Volunteer shift options: trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs are the invented example published with this template (Marrow Creek Community Meals, the Autumn Neighbor Supper). No client data was used. The run was done by an assistant that had not written the template and had not read the example's output beforehand: it followed the instruction block and the output format on the inputs in `public/example.md`, then compared the result with the published output.

## Inputs used

The settings, role list, availability replies, qualification records and assignments in the section "The inputs" of `public/example.md`, unchanged.

## What came out

```
VOLUNTEER SHIFT OPTIONS: Autumn Neighbor Supper, Saturday 2026-12-05

For: Noor Hale, volunteer lead. Prepared Tuesday 2026-11-10 from 5 role rows (13 places), 11 availability replies, 4 qualification records, 2 assignments (1 confirmed, 1 pending). Default shift limit: 2 stated. Limit not stated for: V05, V11. Nothing has been assigned or sent.

Places to fill
S1 Saturday 2026-12-05 09:00-12:00, Setup crew (no requirement): needed 3, confirmed 0, pending 0, to fill 3. Could take it: V01 Alma R., V02 Bruno T., V07 Greta P.
S1 Saturday 2026-12-05 09:00-12:00, Kitchen helper (Food handler card): needed 2, confirmed 0, pending 0, to fill 2. Could take it: V03 Cleo M.
S2 Saturday 2026-12-05 12:00-15:00, Serving line (Food handler card): needed 3, confirmed 0, pending 0, to fill 3. Could take it: V03 Cleo M., V04 Dev K.
S2 Saturday 2026-12-05 12:00-15:00, Greeter (no requirement): needed 2, confirmed 1, pending 0, to fill 1. Could take it: V04 Dev K., V08 Hugo S.
S3 Saturday 2026-12-05 15:00-17:00, Cleanup crew (no requirement): needed 3, confirmed 0, pending 1, to fill 2. Could take it: V01 Alma R., V04 Dev K., V07 Greta P., V10 Jonas B.
Totals: needed 13, confirmed 1, pending 1, to fill 11.
Order used: S1 Kitchen helper (1 could take it), S2 Serving line (2), S2 Greeter (2), S1 Setup crew (3), S3 Cleanup crew (4)

Option 1: Fill the most places
S1 09:00-12:00, Setup crew: placed V01 Alma R., V02 Bruno T., V07 Greta P. Confirmed already: none. Pending: none. Uncovered 0.
S1 09:00-12:00, Kitchen helper: placed V03 Cleo M. Confirmed already: none. Pending: none. Uncovered 1. Why: V03 is the only volunteer who could take this role and is already in this shift. V02 Bruno T. chose it but has no Food handler card on record; V09 Ivy D. chose it but her record is Pending.
S2 12:00-15:00, Serving line: placed V04 Dev K., V03 Cleo M. Confirmed already: none. Pending: none. Uncovered 1. Why: the two volunteers who could take it are both placed. V06 Farid N. chose it but his Food handler card expired before the event; V09 Ivy D. chose it but her record is Pending.
S2 12:00-15:00, Greeter: placed V08 Hugo S. Confirmed already: V07 Greta P. Pending: none. Uncovered 0.
S3 15:00-17:00, Cleanup crew: placed V10 Jonas B., V01 Alma R. Confirmed already: none. Pending: V08 Hugo S. Uncovered 1, of which pending 1. Why: the place is held open for V08's pending confirmation.
Covered 10 of 13 places (confirmed 1, drafted 9). Uncovered 3, of which pending 1.
Not placed: V05 Esme L., hours do not cover; V06 Farid N., requirement not on record; V09 Ivy D., requirement not on record; V11 Kira O., replied not available.

Option 2: One shift each
S1 09:00-12:00, Setup crew: placed V01 Alma R., V02 Bruno T. Confirmed already: none. Pending: none. Uncovered 1. Why: V07 Greta P. could take it but is at the limit (one shift: her confirmed Greeter place). V05 Esme L. chose it but her hours do not cover it.
S1 09:00-12:00, Kitchen helper: placed V03 Cleo M. Confirmed already: none. Pending: none. Uncovered 1. Why: V03 is the only volunteer who could take this role and is already in this shift. V02 Bruno T. has no Food handler card on record; V09 Ivy D.'s record is Pending.
S2 12:00-15:00, Serving line: placed V04 Dev K. Confirmed already: none. Pending: none. Uncovered 2. Why: V03 Cleo M. could take it but is at the limit (placed in Kitchen helper). V06 Farid N.'s card expired before the event; V09 Ivy D.'s record is Pending.
S2 12:00-15:00, Greeter: placed nobody. Confirmed already: V07 Greta P. Pending: none. Uncovered 1. Why: V04 Dev K. (placed in Serving line) and V08 Hugo S. (pending in Cleanup crew) could take it but are at the limit.
S3 15:00-17:00, Cleanup crew: placed V10 Jonas B. Confirmed already: none. Pending: V08 Hugo S. Uncovered 2, of which pending 1. Why: V01 Alma R. (placed in Setup crew), V04 Dev K. (placed in Serving line) and V07 Greta P. (confirmed Greeter) could take it but are at the limit; one place is held open for V08's pending confirmation.
Covered 6 of 13 places (confirmed 1, drafted 5). Uncovered 7, of which pending 1.
Not placed: V05 Esme L., hours do not cover; V06 Farid N., requirement not on record; V09 Ivy D., requirement not on record; V11 Kira O., replied not available.

Flags for the volunteer lead
Pending confirmations: V08 Hugo S., S3 Cleanup crew.
Hours do not cover the shift: V05 Esme L., offered 09:00-11:30, S1 shift 09:00-12:00 (Setup crew), 30 minutes short.
Requirement not on record: V02 Bruno T., S1 Kitchen helper (Food handler card), no record; V06 Farid N., S2 Serving line (Food handler card), expired before the event (valid until 2026-11-30, event 2026-12-05); V09 Ivy D., S1 Kitchen helper and S2 Serving line (Food handler card), status Pending.
Back-to-back shifts in an option: Option 1: V03 Cleo M., S1 Kitchen helper then S2 Serving line; V07 Greta P., S1 Setup crew then S2 Greeter (confirmed); V08 Hugo S., S2 Greeter then S3 Cleanup crew (pending). Option 2: none.
Notes from volunteers, as written: V05 Esme L.: "Can only stay until 11:30"; V07 Greta P.: "Prefers not to work two shifts back to back"; V11 Kira O.: "Away that weekend". The notes have not been applied to either option.
Roles named that are not on the role list: none.
Replied, not available: V11 Kira O.
Over-filled places: none.

Questions for the volunteer lead
1. V08 Hugo S. has a pending assignment for S3 Cleanup crew, so that place is held open and counted as uncovered in both options. Has he confirmed, or should the place be released?
2. V05 Esme L. offered 09:00-11:30 and wrote "Can only stay until 11:30"; Setup crew on S1 runs 09:00-12:00, so she is not in either option. Does a part shift work for this role?
3. V02 Bruno T. chose Kitchen helper, which needs a Food handler card, and there is no record for him. Is there a card that is not in the file?
4. V06 Farid N.'s Food handler card is valid until 2026-11-30, before the event on 2026-12-05. Has it been renewed?
5. V09 Ivy D.'s Food handler card record is Pending. What is its status, and will it be Confirmed before the event?
6. V07 Greta P. wrote "Prefers not to work two shifts back to back". Her confirmed Greeter place is S2 12:00-15:00, and Option 1 puts her in S1 Setup crew 09:00-12:00 as well, which runs straight into it. Does that stand, or should that place stay open?

Draft for Noor Hale's review. Nothing has been assigned, confirmed with a volunteer, sent or changed in any record.
```

## What was observed

- **Every required part was produced:** the header line, places to fill, both options, the flags (all eight kinds, each with "none" where empty), the questions and the closing draft line. The figures add up: 13 places needed, 1 confirmed, 1 pending, 11 to fill; Option 1 covers 10 of 13 with 3 uncovered; Option 2 covers 6 of 13 with 7 uncovered. These match the figures the template's first acceptance test expects.
- **Nothing in the run called for a stop.** The headers, dates and times matched, and no file contradicted another, so there was nothing to stop and ask about. The stop conditions were not exercised.
- **The places, the order, who was placed and the flags matched the published example.** The same volunteers were placed in the same places in both options, the same four were left unplaced in Option 1, and the same flags were raised.
- **Differences from the published example:**
  - Dates. The output format says only "weekday date". I wrote 2026-12-05 beside the weekday, as in the inputs; the example writes "5 December 2026".
  - The header line. The format says "stated / not supplied, 2 used". I wrote "2 stated"; the example writes only "2".
  - Reasons for uncovered places. Mine name each volunteer and the cause in full sentences; the example is shorter and refers to the flags.
  - Option 2, "Not placed". The example lists V07 and V08 as "limit reached". I listed only V05, V06, V09 and V11, because V07 has a confirmed assignment and V08 a pending one and so are already shown against their places. Both readings can be defended from the text.
  - Flags. The example adds that the pending place is held open in both options and that Option 1 also places V08 in Greeter; mine states the pending confirmation only. The example adds "(no hours given)" for V11; mine does not.
  - Questions. I wrote six, one for each pending confirmation, hours flag, requirement flag and note that bears on an option (V05's note and hours flag together). The example wrote four, grouping the three requirement flags into one question.
  - Order line. The example ends it with a full stop; I did not.
- **Facts not in the inputs.** Both outputs call the volunteers "he" or "she" in places, and the inputs give only names; mine used "his" for Farid and Hugo and "her" for Greta, Ivy and Esme. The example does this too ("his pending S3 Cleanup crew"). Apart from that, every figure and name in both outputs comes from the inputs. The example labels Noor Hale "Volunteer Lead" with capitals, which is a small change from the inputs.

## Ambiguities and shortcomings in the template

- "Weekday date" in the output format does not say how to write the date, so two correct runs will differ.
- Whether a volunteer with a confirmed or pending assignment, who is at the limit, appears under "Not placed" with "limit reached" is not settled. Step 8 says to use it for a volunteer who "could have taken a place but whose limit stopped them", which fits V07 and V08; the checklist says every volunteer appears as placed, confirmed, pending or not placed.
- "Limit not stated for" includes V11, who replied as not available and so has no use for a limit. The template does not say whether to list them.
- The reason "positions filled" is defined in step 8 but was never needed on this example, so it was not tested.
- The step that writes questions says "one for each" flag but does not say whether several volunteers with the same kind of flag share a question. The example groups them; the text reads as separate questions.
- The instruction block's tie-break "fewest shifts so far" counts a Pending assignment toward the volunteer's shifts, which matters here for V08. This is stated, but a reader could miss it.
- The "free" test says "no Confirmed or Pending assignment in that shift". That is why V07 does not appear as able to take a second Greeter place, which is correct, but it took care to apply.
- No gendered wording is called for by the inputs, and the template does not warn against it.
- The template's version notes still say it has not been tried in a named AI product. That is out of date as of this record.

## Edits after this run

The record above is of the run as it happened, and it has not been changed. The template and the example were edited afterwards and the template was not run again: Option 1 was renamed from "Fill the most places" to "Fill as many places as the order allows"; the example's date style, header line, wording about volunteers (no pronouns), "(no hours given)" for V11, role title and questions were brought into line with the template; the list of volunteers not placed is now headed "Not placed in this draft"; and three rules were added to the instruction block. Where this record differs from the current `public/example.md` or `member/template.md`, the edits are the reason. Acceptance tests 2 to 14 have not been run.
