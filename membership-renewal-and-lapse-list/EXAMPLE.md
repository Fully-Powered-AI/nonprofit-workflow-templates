# Membership renewal and lapse list: an example

*Illustrative example with sample data.* The organization, its members, its staff and every figure below are illustrative. Arts Society A is an illustrative community arts association with three membership levels. First come the inputs the membership coordinator supplied, in full: the member export from the membership management system, the society's renewal rules, its approved facts for each level and today's date. Then the list the workflow template returned.

## The inputs

```
MEMBER EXPORT (from the membership management system, taken Monday 2 November 2026)
member_id | name               | membership_level | joined_at  | renewal_date | status    | auto_renew | last_payment_at | contact_preference | do_not_contact
M-1001    | Odile Fenwick      | Individual       | 2021-03-14 | 2026-11-20   | active    | no         | 2025-11-18      | email              | no
M-1002    | Tomas Arkwright    | Household        | 2019-11-25 | 2026-11-25   | active    | yes        | 2025-11-25      | email              | no
M-1003    | Bea Okonkwo-Lind   | Supporter        | 2023-12-01 | 2026-12-01   | active    | no         | 2025-12-01      | post               | no
M-1004    | Halvard Pereira    | Individual       | 2024-10-15 | 2026-10-15   | active    | no         | 2025-10-15      | phone              | no
M-1005    | Signe Ballantyne   | Household        | 2022-10-20 | 2026-10-20   | active    | yes        | 2025-10-20      | email              | no
M-1006    | Ravi Castellano    | Individual       | 2025-09-12 | 2026-09-12   | lapsed    | no         | 2025-09-12      | email              | no
M-1007    | Juno Whitcombe     | Supporter        | 2020-09-05 | 2026-09-05   | active    | no         | 2025-09-05      | post               | no
M-1008    | Esme Tolliver      | Individual       | 2023-08-10 | 2026-08-10   | lapsed    | no         | 2025-08-10      | email              | no
M-1009    | Caspar Lindqvist   | Household        | 2018-11-28 | 2026-11-28   | active    | no         | 2025-11-28      | email              | yes
M-1010    | Wanda Achterberg   | Individual       | 2025-05-03 | 2027-05-03   | active    | no         | 2026-05-03      | email              | no
M-1011    | Nils Okafor        | Supporter        | 2021-02-17 | 2027-02-17   | active    | yes        | 2026-02-17      | email              | no
M-1012    | Ida Marchetti      | Individual       | 2024-06-30 |              | active    | no         | 2025-06-30      | email              | no
M-1013    | Felix Durand-Shaw  | Household        | 2025-11-30 | 2026-11-31   | active    | no         | 2025-11-30      | email              | no
M-1014    | Greta Holm         | Individual       | 2022-07-01 | 2026-07-01   | cancelled | no         | 2025-07-01      | email              | no
M-1015    | Ottilie Brandvold  | Supporter        | 2024-10-28 | 2026-10-28   | active    | no         | 2026-10-29      | email              | no

RENEWAL RULES
Reminder window: 30 days before the renewal date
Grace period: 30 days after the renewal date
Last run: 2026-10-01
Organization name: Arts Society A
Subject line, reminders: Your Arts Society A membership renewal
Subject line, lapsed notes: Your Arts Society A membership
Reminders, all levels: signed by Rosalind Kerr, Membership coordinator
Lapsed notes, Individual and Household: signed by Rosalind Kerr, Membership coordinator
Lapsed notes, Supporter: signed by Mateo Ferris, Chair

APPROVED FACTS (owner: membership lead; reviewed 1 October 2026; each line is used unchanged)
All levels
  How to renew: Renew on the members' page of our website, by cheque to the society office, or in person at the front desk.
  How to rejoin: Rejoin on the members' page of our website, by cheque to the society office, or in person at the front desk.
  Questions: membership@example.org or 555-0142, weekdays 10am to 4pm.
  Welcome-back line: You are welcome back at any time, and rejoining costs the same as renewing.
Individual
  Fee: Individual membership is $60 for the year.
  Includes: It includes the members' rate on every class, the quarterly newsletter and a vote at the annual meeting.
Household
  Fee: Household membership is $95 for the year, for up to two adults and their children at one address.
  Includes: It includes the members' rate on every class for each of them, the quarterly newsletter and two votes at the annual meeting.
Supporter
  Fee: Supporter membership is $150 for the year.
  Includes: It includes everything in Individual membership and two guest passes to the spring exhibition.

TODAY'S DATE
2026-11-02
```

## The output

```
MEMBERSHIP RENEWAL AND LAPSE LIST: Arts Society A, November 2026
Status: Draft for Rosalind Kerr, Membership coordinator. Nothing has been sent, no payment taken and no record changed.
Run: today 2026-11-02. Last run 2026-10-01 (supplied). Reminder window 30 days (renewal dates 2026-11-02 to 2026-12-02). Grace period 30 days.

TOTALS
Export rows 15 = Due, reminder 3 + Due, auto-renew on 1 + In the grace period 2 + Lapsed since the last run 2 + Lapsed before the last run 1 + Not yet due 2 + Cancelled 1 + Records to check 3.

1. DUE TO RENEW, REMINDER (3)
- M-1001, Odile Fenwick, Individual. Renews 2026-11-20, in 18 days. Email.
- M-1003, Bea Okonkwo-Lind, Supporter. Renews 2026-12-01, in 29 days. Post.
- M-1009, Caspar Lindqvist, Household. Renews 2026-11-28, in 26 days. Do not contact: no message.

2. DUE TO RENEW, AUTO-RENEW ON (1). No reminder drafted.
- M-1002, Tomas Arkwright, Household. Renews 2026-11-25, in 23 days.

3. IN THE GRACE PERIOD (2)
- M-1004, Halvard Pereira, Individual. Was due 2026-10-15, 18 days ago. Open until 2026-11-14. Phone: use the draft as call notes.
- M-1005, Signe Ballantyne, Household. Was due 2026-10-20, 13 days ago. Open until 2026-11-19. Email. Auto-renew is on but the renewal date has passed; check why before any reminder is used.

4. LAPSED SINCE THE LAST RUN (2)
- M-1006, Ravi Castellano, Individual. Was due 2026-09-12. Lapsed 2026-10-13. Status in the system: lapsed. Email.
- M-1007, Juno Whitcombe, Supporter. Was due 2026-09-05. Lapsed 2026-10-06. Status in the system: active. Post. Still marked active in the system.

5. RECORDS TO CHECK (3). Nothing drafted.
- M-1012, Ida Marchetti. renewal_date: blank.
- M-1013, Felix Durand-Shaw. renewal_date: 2026-11-31 is not a real date.
- M-1015, Ottilie Brandvold. last_payment_at: 2026-10-29 is after the renewal date of 2026-10-28, and the renewal date has not moved; the member may already have renewed.

6. LEFT OUT, AND WHY
- Do not contact: M-1009, Caspar Lindqvist, Due, reminder.
- Cancelled: M-1014, Greta Holm.
- Lapsed before the last run, already listed: M-1008, Esme Tolliver, lapsed 2026-09-10.
- Records to check: see section 5.
- Not yet due: 2, counted only.

7. DRAFT RENEWAL REMINDERS
Individual. For: M-1001 (due), M-1004 (grace). Signed by: Rosalind Kerr, Membership coordinator.
Subject: Your Arts Society A membership renewal
Dear [name],
[Due: Your Individual membership renews on [renewal date].]
[Grace: Your Individual membership was due for renewal on [renewal date]. It stays open until [open until].]
Individual membership is $60 for the year. It includes the members' rate on every class, the quarterly newsletter and a vote at the annual meeting.
Renew on the members' page of our website, by cheque to the society office, or in person at the front desk.
Questions: membership@example.org or 555-0142, weekdays 10am to 4pm.
Rosalind Kerr, Membership coordinator

Household. For: M-1005 (grace; check the auto-renew note first). Signed by: Rosalind Kerr, Membership coordinator.
Subject: Your Arts Society A membership renewal
Dear [name],
[Grace: Your Household membership was due for renewal on [renewal date]. It stays open until [open until].]
Household membership is $95 for the year, for up to two adults and their children at one address. It includes the members' rate on every class for each of them, the quarterly newsletter and two votes at the annual meeting.
Renew on the members' page of our website, by cheque to the society office, or in person at the front desk.
Questions: membership@example.org or 555-0142, weekdays 10am to 4pm.
Rosalind Kerr, Membership coordinator

Supporter. For: M-1003 (due). Signed by: Rosalind Kerr, Membership coordinator.
Subject: Your Arts Society A membership renewal
Dear [name],
[Due: Your Supporter membership renews on [renewal date].]
Supporter membership is $150 for the year. It includes everything in Individual membership and two guest passes to the spring exhibition.
Renew on the members' page of our website, by cheque to the society office, or in person at the front desk.
Questions: membership@example.org or 555-0142, weekdays 10am to 4pm.
Rosalind Kerr, Membership coordinator

8. DRAFT LAPSED-MEMBER NOTES
Individual. For: M-1006. Signed by: Rosalind Kerr, Membership coordinator.
Subject: Your Arts Society A membership
Dear [name],
Your Individual membership was due for renewal on [renewal date], and its grace period has now passed.
You are welcome back at any time, and rejoining costs the same as renewing.
Individual membership is $60 for the year. It includes the members' rate on every class, the quarterly newsletter and a vote at the annual meeting.
Rejoin on the members' page of our website, by cheque to the society office, or in person at the front desk.
Questions: membership@example.org or 555-0142, weekdays 10am to 4pm.
Rosalind Kerr, Membership coordinator

Household. No lapsed member this month; no note drafted.

Supporter. For: M-1007. Signed by: Mateo Ferris, Chair.
Subject: Your Arts Society A membership
Dear [name],
Your Supporter membership was due for renewal on [renewal date], and its grace period has now passed.
You are welcome back at any time, and rejoining costs the same as renewing.
Supporter membership is $150 for the year. It includes everything in Individual membership and two guest passes to the spring exhibition.
Rejoin on the members' page of our website, by cheque to the society office, or in person at the front desk.
Questions: membership@example.org or 555-0142, weekdays 10am to 4pm.
Mateo Ferris, Chair

CHECK
Every fact in the drafts is from the approved facts: yes. Drafts are the same for every member of a level apart from the merge fields. No draft goes to a member marked do not contact.
Prepared for Rosalind Kerr, Membership coordinator. The assistant has sent nothing, taken no payment and changed no record.
```

How the dates were placed: today is 2026-11-02, so the reminder window runs to 2026-12-02 and a renewal date between 2026-10-03 and 2026-11-01 is inside the 30-day grace period. A member lapses on the renewal date plus 31 days; Ravi Castellano and Juno Whitcombe lapsed after the last run on 2026-10-01, and Esme Tolliver lapsed before it. Greta Holm is left out because her membership was cancelled. Wanda Achterberg and Nils Okafor renew in 2027 and are counted as not yet due. Every figure traces to the export, the renewal rules and the approved facts above.
