# Membership renewal and lapse list

Workflow template, version 0.1.0.

## Purpose

Prepare the month's membership list from the member export: who is due to renew inside the reminder window (with auto-renewing members kept apart), who is inside the grace period, who has lapsed since the last run, and which records carry a missing or impossible date. Every group is counted, and the counts add back to the number of rows in the export. For each membership level that needs one, draft a renewal reminder and a lapsed-member note built only from the organization's approved facts, and list everyone left out with the reason. The assistant prepares; it never sends a message, takes a payment, changes a status or cancels a membership. A person approves and sends.

## When to use it and when not to

Use it once a month, on the day the membership coordinator works through renewals, after taking a fresh export from the membership system.

Do not use it:

- to thank a donor for a gift. Donor thank-you drafts covers that, and a gift is not a membership fee;
- for customer accounts of a business coming up for renewal. Renewal risk review covers those;
- to decide who is worth chasing, to rank members, or to guess what anyone could afford. Every member at a level gets the same draft;
- to change a member's status, take or retry a payment, or cancel anyone. Those are done by a person in the membership system;
- when the export has no do_not_contact column or no renewal_date column, because the list cannot be made safely without them.

## Roles

- **Runs it:** the membership coordinator or membership administrator.
- **Reads the list, edits the drafts, approves and sends every message:** the membership coordinator, or whoever the organization's renewal rules name as the writer for that level.
- **Decides what to do about each record to check, and changes any status in the system:** the person who keeps the membership records (often the coordinator).
- **Owns the approved facts for each level (fee, what membership includes, how to renew):** the membership lead, or whoever the organization names.

## Inputs

1. **The member export from your membership management system.** One row per member. Default column headers: member_id, name, membership_level, joined_at, renewal_date, status, auto_renew, last_payment_at, contact_preference, do_not_contact. Dates are written YYYY-MM-DD. status is one of active, lapsed, cancelled. auto_renew and do_not_contact are yes or no. contact_preference is email, post or phone. If a header does not match, stop and ask which supplied column stands for it; never guess. If a member_id appears twice, stop and ask which row is right.
2. **The organization's renewal rules.**
   - The reminder window: how many days ahead of the renewal date a reminder goes. Default 30 days.
   - The grace period: how many days after the renewal date a membership stays open before the member counts as lapsed. Default 30 days.
   - Who writes to whom: the signer, with title, for reminders and for lapsed notes at each level. If no signer is named for a level, stop and ask.
   - The date of the last run. Default: the same day of the previous month, stated in the header.
   - The organization's name, for the heading.
   - The subject line for reminders and the subject line for lapsed notes, each a finished line the drafts use unchanged. If none is given, the drafts show [subject] for the coordinator to fill in; the assistant does not write one.
3. **The approved facts for each level.** For each membership level: its name exactly as the export writes it, a sentence giving the fee for the year, and a sentence on what membership includes. For all levels, or per level: a sentence on how to renew, a sentence on how to rejoin, where to ask questions, and any approved welcome-back line for lapsed members. Each is a finished sentence the drafts use unchanged. The assistant uses nothing else about a level. If a level has no fee or no includes sentence, treat it as having no approved facts. If no rejoin sentence is given, use the renewal sentence unchanged.
4. **Today's date.** If it is not supplied, stop and ask. Do not take the date from anywhere else.

The assistant works from the files and notes the person supplies. It needs no connection to the membership system or to any mail or payment system, and never asks for a password or a login code.

## The procedure

Write T for today, W for the reminder window, G for the grace period and L for the date of the last run. "Days to renewal" is renewal_date minus T, counted in calendar days.

1. **Check the inputs.** Confirm every header. Count the export rows; this is the total every group must add back to. If a member_id repeats, stop on it.
2. **Set aside cancelled members.** A row whose status is cancelled goes to Cancelled. It is counted and named under Left out, gets no message, and is not checked further.
3. **Find records to check.** Every other row goes to Records to check, with the field and the problem, if any of these holds:
   1. renewal_date or joined_at is blank, or is not a real calendar date (for example 2026-11-31);
   2. joined_at is later than T, or renewal_date is on or before joined_at;
   3. last_payment_at is later than T, or is not a real date (a blank last_payment_at is allowed);
   4. last_payment_at is later than renewal_date: a payment was recorded after the renewal date, but the date has not moved, so the member may already have renewed;
   5. status is lapsed but renewal_date is on or after T;
   6. status, auto_renew, do_not_contact or contact_preference holds a value outside its list (a blank contact_preference is allowed and is not a problem; see step 8).
   A record to check gets no message. Name every problem found on the row. If the row is also marked do not contact, it stays in Records to check, which comes first, and is also named under Left out as do not contact.
4. **Place every remaining row in exactly one date group.**
   1. Days to renewal greater than W: **Not yet due.** Counted only, not named.
   2. Days to renewal from 0 to W: **Due to renew.** If auto_renew is yes, it goes to Due, auto-renew on, with no reminder. If auto_renew is no, it goes to Due, reminder.
   3. Days to renewal from minus G to minus 1: **In the grace period.** The membership stays open until renewal_date plus G days; show that date.
   4. Days to renewal less than minus G: lapsed. The member lapsed on renewal_date plus G plus 1 day. If that day is later than L, the member goes to **Lapsed since the last run**. If it is L or earlier, the member goes to **Lapsed before the last run**: counted and named under Left out, with no new message, because the last run already listed them. A member who lapsed on L itself is in that group, because the last run, made on L, already counted them.
5. **Add notes where the record and the dates disagree.** Do not move the row and do not change anything in the system.
   - In the grace period with auto_renew yes: "auto-renew is on but the renewal date has passed; check why before any reminder is used." The member still counts toward the level's reminder and the draft is made; the coordinator decides whether to use it.
   - In the grace period with status lapsed: "marked lapsed in the system before the grace period ended."
   - Lapsed since the last run with status active: "still marked active in the system."
   - Lapsed before the last run with status active: the same note, "still marked active in the system," shown beside the member under Left out.
6. **Apply contact rules.** A member with do_not_contact yes stays in their group and is counted there, but is marked "do not contact: no message" and is also named under Left out. Nobody marked do not contact is given a draft, whatever their group.
7. **Check the approved facts.** For each level that has at least one contactable member in Due, reminder, or In the grace period, a reminder is needed. For each level that has at least one contactable member in Lapsed since the last run, a lapsed note is needed. If a level that needs a draft has no approved facts, or the export spells it differently from the approved facts, write no draft for it, say so in the drafts section, and mark its members "no draft: no approved facts for this level."
8. **Show the channel.** Beside each contactable member, show the contact_preference: email, post or phone. For phone, write "phone: use the draft as call notes". If contact_preference is blank, write "channel not stated: the coordinator decides".
9. **Draft one renewal reminder per level that needs one.** Use merge fields in square brackets for what changes per member: [name], [renewal date] and, for the grace period, [open until]. The draft holds, in this order: the subject line from the renewal rules, word for word, or [subject] if none was given; "Dear [name],"; for Due members, a sentence that their [level] membership renews on [renewal date]; for grace-period members, the alternative sentence "Your [level] membership was due for renewal on [renewal date]. It stays open until [open until]."; the level's fee sentence and includes sentence, word for word; the renewal sentence; the questions line; the signer from the renewal rules. Include only the Due or grace sentence the level's members need; if both are needed, show both, each marked. Add nothing else: no urgency, no discount, no claim about what the organization has achieved, no comment about the member, and no wording that differs between members of the same level.
10. **Draft one lapsed-member note per level that needs one.** Same merge fields, without [open until]. The draft opens with the subject line for lapsed notes (or [subject]) and "Dear [name],", then says "Your [level] membership was due for renewal on [renewal date], and its grace period has now passed."; places the approved welcome-back line, if there is one, unchanged; repeats the level's fee and includes sentences word for word; places the rejoin sentence; and gives the questions line and the signer for lapsed notes at that level. No guilt, no pressure, no deadline the approved facts do not give.
11. **Tie out.** Total rows = Due, reminder + Due, auto-renew on + In the grace period + Lapsed since the last run + Lapsed before the last run + Not yet due + Cancelled + Records to check. If it does not add up, stop, report the figures and draft nothing.

## Exceptions and stop conditions

- **A header does not match, today's date is missing, or a level that needs a draft has no named signer:** stop and ask.
- **A member_id appears twice:** stop on that member_id and ask which row is right.
- **The groups do not add back to the number of export rows:** stop, report each count and the difference, and draft nothing.
- **A level in the export is missing from the approved facts:** no draft for that level; its members are listed with the reason.
- **Asked to send a message, take or retry a payment, change a status, cancel a member, or remove someone from the list:** decline. A person does those in the membership system.
- **Asked to rank members, pick out those "worth" chasing, guess what a member could pay or give, or write differently to some members of a level:** decline. Every member of a level gets the same draft.
- **Asked to add a fact, benefit, figure or deadline that is not in the approved facts:** decline and say which fact is missing.
- **Asked to write to a member marked do not contact:** decline.

## Output format

```
MEMBERSHIP RENEWAL AND LAPSE LIST: [Organization], [month and year]
Status: Draft for [coordinator]. Nothing has been sent, no payment taken and no record changed.
Run: today [T]. Last run [L] ([supplied, or default: same day last month]). Reminder window [W] days (renewal dates [T] to [T + W]). Grace period [G] days.

TOTALS
Export rows [n] = Due, reminder [n] + Due, auto-renew on [n] + In the grace period [n] + Lapsed since the last run [n] + Lapsed before the last run [n] + Not yet due [n] + Cancelled [n] + Records to check [n].

1. DUE TO RENEW, REMINDER ([n])
- [member_id], [name], [level]. Renews [date], in [n] days. [Channel, or "do not contact: no message"]. [Note, if any]
[If none, write "None."]

2. DUE TO RENEW, AUTO-RENEW ON ([n]). No reminder drafted.
- [member_id], [name], [level]. Renews [date], in [n] days.
[If none, write "None."]

3. IN THE GRACE PERIOD ([n])
- [member_id], [name], [level]. Was due [date], [n] days ago. Open until [date]. [Channel, or "do not contact: no message"]. [Note, if any]
[If none, write "None."]

4. LAPSED SINCE THE LAST RUN ([n])
- [member_id], [name], [level]. Was due [date]. Lapsed [date]. Status in the system: [status]. [Channel, or "do not contact: no message"]. [Note, if any]
[If none, write "None."]

5. RECORDS TO CHECK ([n]). Nothing drafted.
- [member_id], [name]. [Field]: [what is wrong].
[If none, write "None."]

6. LEFT OUT, AND WHY
- Do not contact: [member_id, name, group] or "None."
- Cancelled: [member_id, name] or "None."
- Lapsed before the last run, already listed: [member_id, name, lapsed date, note if any] or "None."
- Records to check: see section 5.
- Not yet due: [n], counted only.

7. DRAFT RENEWAL REMINDERS
[Level]. For: [member_ids, each followed by (due) or (grace), or (grace; check the auto-renew note first) where that note applies]. Signed by: [signer, title].
Subject: [subject]
Dear [name],
[Due: Your [level] membership renews on [renewal date].]   (only if the level has Due members)
[Grace: Your [level] membership was due for renewal on [renewal date]. It stays open until [open until].]   (only if the level has grace members)
[Fee sentence, word for word.] [Includes sentence, word for word.]
[Renewal sentence, word for word.]
[Questions line, word for word.]
[Signer]
[Repeat for each level. For a level with no draft needed or no approved facts, one line saying which.]

8. DRAFT LAPSED-MEMBER NOTES
[Level]. For: [member_ids]. Signed by: [signer, title].
Subject: [subject]
Dear [name],
[Your [level] membership was due for renewal on [renewal date], and its grace period has now passed.]
[Approved welcome-back line, if any, word for word.]
[Fee sentence, word for word.] [Includes sentence, word for word.]
[Rejoin sentence, word for word.]
[Questions line, word for word.]
[Signer]
[Repeat for each level. For a level with no draft needed or no approved facts, one line saying which.]

CHECK
Every fact in the drafts is from the approved facts: [yes, or name the gap]. Drafts are the same for every member of a level apart from the merge fields. No draft goes to a member marked do not contact.
Prepared for [coordinator]. The assistant has sent nothing, taken no payment and changed no record.
```

## Reviewer checklist

1. The totals line adds up and its first figure equals the rows in the export. (Membership coordinator)
2. Every date group is right for today's date, the reminder window and the grace period; spot-check three rows by hand. (Membership coordinator)
3. Nobody marked do not contact, cancelled or lapsed before the last run has a draft. (Membership coordinator)
4. Every record to check names the field and the problem, and none has a draft. (Records keeper)
5. Each draft's fee, benefits and renewal route match the approved facts word for word. (Membership lead)
6. Each draft is signed by the person the renewal rules name for that level and kind of message. (Membership lead)
7. No draft ranks, singles out or comments on any member. (Membership lead)

## Acceptance tests

Proposed tests. None has been run.

1. **Normal month.** Fifteen rows across every group, today 2026-11-02, last run 2026-10-01, window 30, grace 30. Expected: the totals line reads 15 and every row is in one group.
2. **Header mismatch.** The export calls the column "expires_on" instead of renewal_date. Expected: stops and asks which column stands for renewal_date.
3. **Impossible date.** renewal_date 2026-11-31. Expected: under Records to check, no draft.
4. **Payment after the renewal date.** renewal_date 2026-10-28, last_payment_at 2026-10-29. Expected: under Records to check as possibly renewed, not in the grace period.
5. **Auto-renew in grace.** auto_renew yes and renewal_date 13 days ago. Expected: in the grace period with the auto-renew note.
6. **Lapsed before the last run.** renewal_date 2026-08-10, grace 30, last run 2026-10-01. Expected: lapsed on 2026-09-10, listed under Left out, no lapsed note.
7. **Do not contact.** A due member with do_not_contact yes. Expected: counted in Due, reminder, marked "do not contact: no message", named under Left out.
8. **Level with no approved facts.** A member at a level the facts do not list. Expected: no draft for that level, with the reason.
9. **Asked to rank.** "Put the members most worth keeping first." Expected: declined.
10. **Asked to update statuses.** "Mark the lapsed members as lapsed." Expected: declined; it changes no record.

## Instructions for the AI assistant

```
You prepare the monthly membership renewal and lapse list for a membership
coordinator. You never send a message, take or retry a payment, change a
status, cancel a member or write to anyone marked do not contact. A person
approves and sends every message.

The user will supply: the member export (default headers: member_id, name,
membership_level, joined_at, renewal_date, status, auto_renew,
last_payment_at, contact_preference, do_not_contact; dates YYYY-MM-DD;
status active, lapsed or cancelled; auto_renew and do_not_contact yes or
no; contact_preference email, post or phone); the renewal rules (reminder
window W, default 30 days; grace period G, default 30 days; the signer for
reminders and lapsed notes at each level; the last run date L, default the
same day last month); the approved facts (per level: name, fee sentence,
includes sentence; and renewal sentence, rejoin sentence, questions
line, any welcome-back line); the organization's name; the subject line
for reminders and for lapsed notes; and today's date T. If a header does
not match, T is missing, or a level needing a draft has no signer, stop
and ask. If no subject line is given, write [subject] in its place; never
invent one. Never ask for a password or a login code.

1. Count the export rows. If a member_id repeats, stop on it.
2. status cancelled: group Cancelled, no message, no further checks.
3. Records to check, no message, naming every problem: renewal_date or
   joined_at blank or not a real date; joined_at after T; renewal_date on
   or before joined_at; last_payment_at after T or not a real date (blank
   is allowed); last_payment_at after renewal_date (may have renewed);
   status lapsed with renewal_date on or after T; any value outside its list
   (blank contact_preference is allowed). A row with a problem and do not
   contact yes stays here and is also named under Left out.
4. Days to renewal = renewal_date minus T. Over W: Not yet due (count
   only). 0 to W: Due, auto-renew on if auto_renew is yes (no reminder),
   else Due, reminder. Minus G to minus 1: In the grace period, open until
   renewal_date plus G. Below minus G: lapsed on renewal_date plus G plus
   1; if that is after L, Lapsed since the last run; if it is L or
   earlier, Lapsed before the last run (named under Left out, no message).
5. Notes, without moving the row: grace with auto_renew yes: "auto-renew
   is on but the renewal date has passed; check why before any reminder is
   used" (still drafted for, and the coordinator decides whether to use
   it); grace with status lapsed: "marked lapsed in the system before the
   grace period ended"; lapsed since the last run or before it with status
   active: "still marked active in the system" (before the last run, shown
   beside the member under Left out).
6. do_not_contact yes: keep in the group and count there, mark "do not
   contact: no message", name under Left out, never draft for them.
7. Show each contactable member's channel; phone means "use the draft as
   call notes"; blank means "channel not stated: the coordinator decides".
8. One renewal reminder per level with a contactable member in Due,
   reminder or the grace period; one lapsed note per level with a
   contactable member lapsed since the last run. Use merge fields [name],
   [renewal date], [open until]. Use only the approved sentences, word
   for word; show only the Due or grace sentence a level needs. The Due
   sentence is "Your [level] membership renews on [renewal date]." The
   grace sentence is "Your [level] membership was due for renewal on
   [renewal date]. It stays open until [open until]." In a reminder's For
   line, follow each member_id with (due) or (grace), or with (grace; check
   the auto-renew note first) where that note applies. Reminder order:
   subject line, "Dear [name],", Due or grace sentence, fee, includes,
   renewal sentence, questions line, signer. Lapsed note order: subject
   line, "Dear [name],", "Your [level] membership was due for renewal on
   [renewal date], and its grace period has now passed.", welcome-back line
   if any, fee, includes, rejoin sentence, questions line, signer. No
   rejoin sentence: use the renewal sentence. No urgency, discount,
   achievement, comment on a member, or wording that differs between
   members of a level. No approved facts for a level: no draft, say why.
9. Tie out: the eight group counts must add to the export rows. If not,
   stop, report the counts and the difference, and draft nothing.
10. Use the output format exactly. Where a section is empty, write
    "None." End with the check lines and the closing line.

Decline to rank members, judge anyone's worth or what they could pay or
give, add facts, change records or send anything.
```

Paste this block as custom instructions, followed by the output format above.

## What to customize

- The reminder window, the grace period and the day of the month the list is made.
- Your column headers, if your membership system names them differently.
- Your membership levels and their approved sentences: fee, what membership includes, how to renew, how to rejoin, where to ask, and any welcome-back line, each with an owner.
- Who signs reminders and lapsed notes at each level, and the subject lines they carry.
- Whether auto-renewing members should receive an advance notice; by default they get none.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 19 November 2026. Written by FullyPowered AI. Tried on its invented example on 19 November 2026, and the record is published with it; the example's inputs and this block were then edited (an organization name and subject lines added, and some wording made explicit) and the record was rewritten after a second run. Not yet tested in a client environment.
