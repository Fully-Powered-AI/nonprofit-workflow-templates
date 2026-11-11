# Restricted gift rollforward: an invented example

*Illustrative example with invented data.* Cedar Row Youth Arts is an invented small nonprofit. The donors, the account names, the references and every figure below are invented. First come the inputs the bookkeeper supplied, in full, then the schedule the capability returned.

## The inputs

```
SETTINGS
Fund: Studio Access Fund    Fund code: SAF
Period: 2026-10-01 to 2026-10-31    Currency: USD
Finance lead role: Finance Lead    Run date: 2026-11-09

GIFT AGREEMENT SUMMARY (written by the Finance Lead)
Agreement ref | Donor        | Fund | Stated use                                                  | Start date | End date   | Amount stated
AG-01         | Foundation A | SAF  | Free studio sessions and materials for young people from low-income households | 2026-01-01 | 2026-12-31 | 60000.00
AG-02         | Donor B      | SAF  | Teaching-artist fees for the Saturday sessions              | 2026-07-01 | 2027-06-30 | 24000.00
AG-03         | Donor C      | SAF  | Art supplies for the access program                         | 2026-10-01 |            | 2000.00

APPROVED FUND CODING (approved by the Finance Lead)
Account | Account name           | Status
6100    | Teaching-artist fees   | Within stated use
6200    | Art supplies           | Within stated use
6300    | Studio rent            | Confirm
6400    | Marketing and printing | Outside stated use

LEDGER DETAIL (export, run 2026-11-09; amounts increase the fund when positive)
Date       | Reference | Description                       | Account | Fund | Entry type | Amount   | Agreement ref
2026-10-02 | GL-5101   | Gift, Foundation A, instalment 3  | 4100    | SAF  | Gift       | 5000.00  | AG-01
2026-10-05 | GL-5107   | Gift, Donor B, instalment         | 4100    | SAF  | Gift       | 2000.00  | AG-02
2026-10-06 | GL-5110   | Saturday session teaching fees    | 6100    | SAF  | Expense    | -2400.00 |
2026-10-09 | GL-5112   | Gift, Donor C                     | 4100    | SAF  | Gift       | 1500.00  | AG-03
2026-10-12 | GL-5120   | Gift, Donor D                     | 4100    | SAF  | Gift       | 250.00   |
2026-10-13 | GL-5118   | Clay and paper order              | 6200    | SAF  | Expense    | -860.50  |
2026-10-13 | GL-5119   | Clay and paper order              | 6200    | SAF  | Expense    | -860.50  |
2026-10-14 | GL-5116   | Gala tickets                      | 4200    | GEN  | Gift       | 900.00   |
2026-10-15 | GL-5122   | Studio rent, October              | 6300    | SAF  | Expense    | -1800.00 |
2026-10-19 | GL-5127   | Flyers for open day               | 6400    | SAF  | Expense    | -340.00  |
2026-10-21 | GL-5133   | Gift, Donor C, second gift        | 4100    | SAF  | Gift       | 800.00   | AG-03
2026-10-23 | GL-5136   | Software subscription             | 7200    | SAF  | Expense    | -65.00   |
2026-10-27 | GL-5140   | Clay and paper order, refund      | 6200    | SAF  | Expense    | 120.00   |
2026-10-28 | GL-5142   | Transfer to General Fund, per treasurer note | 9100 | SAF | Transfer | -500.00 |
2026-11-02 | GL-5150   | Gift, Donor C                     | 4100    | SAF  | Gift       | 300.00   | AG-03

BALANCES
Prior reconciled balance, SAF, at 2026-09-30: 41250.00, reconciled by the Bookkeeper
Ledger balance, SAF, at the start of the period: 41350.00
Ledger balance, SAF, at 2026-10-31: 44244.00
```

## The output

```
RESTRICTED GIFT ROLLFORWARD: Studio Access Fund (SAF), 2026-10-01 to 2026-10-31

For: Finance Lead. Working schedule. Nothing has been posted, coded or changed. Amounts in USD; an increase in the fund is positive.
Prepared: 2026-11-09, from the agreement summary (3 agreements), the fund coding (4 accounts), the ledger detail (15 rows) and the balances supplied.

Stated use, as supplied (not interpreted):
AG-01, Foundation A: "Free studio sessions and materials for young people from low-income households". Dates 2026-01-01 to 2026-12-31. Amount stated 60,000.00.
AG-02, Donor B: "Teaching-artist fees for the Saturday sessions". Dates 2026-07-01 to 2027-06-30. Amount stated 24,000.00.
AG-03, Donor C: "Art supplies for the access program". Dates 2026-10-01 to no end stated. Amount stated 2,000.00.

Rollforward:
Opening balance, prior reconciled at 2026-09-30 by the Bookkeeper: 41,250.00
Gifts recorded (5): +9,550.00
Expenditure (7): -6,206.00
Transfers and adjustments (1): -500.00
Computed closing balance: 44,094.00
Ledger balance at 2026-10-31: 44,244.00
Difference, ledger less computed: +150.00. Opening difference +100.00 (ledger balance at the start of the period 41,350.00 less prior reconciled 41,250.00). Movement difference +50.00 (the ledger moved 2,894.00; the detail rows total 2,844.00).

Gifts recorded, by agreement:
AG-01: 1 gift, 5,000.00. GL-5101. Inside the agreement's dates.
AG-02: 1 gift, 2,000.00. GL-5107. Inside the agreement's dates.
AG-03: 2 gifts, 2,300.00. GL-5112, GL-5133. Inside the agreement's dates.
No agreement reference: 1 gift, 250.00. GL-5120.
Total gifts: 9,550.00.

Expenditure, by the finance lead's coding:
Within stated use: 4 rows, -4,001.00. Teaching-artist fees (6100): -2,400.00 (GL-5110). Art supplies (6200): -1,601.00 (GL-5118, GL-5119, GL-5140).
Outside stated use: 1 row, -340.00. Marketing and printing (6400): -340.00 (GL-5127).
To confirm: 1 row, -1,800.00. Studio rent (6300): -1,800.00 (GL-5122).
Account not in the coding table: 1 row, -65.00. Account 7200: -65.00 (GL-5136).
Total expenditure: -6,206.00.

Transfers and adjustments:
GL-5142, 2026-10-28, Transfer to General Fund, per treasurer note: -500.00.

Unresolved differences: 10
1. Opening difference, +100.00. The ledger balance at the start of the period is 41,350.00; the prior reconciled balance is 41,250.00. Who can answer: the Bookkeeper. The Finance Lead decides.
2. Movement difference, +50.00. The ledger moved 2,894.00 in the period; the detail rows in the schedule total 2,844.00. Who can answer: the Bookkeeper. The Finance Lead decides.
3. Gifts above the amount stated. AG-03: GL-5112 (1,500.00) and GL-5133 (800.00) total 2,300.00 in this period; the summary states 2,000.00, an excess of 300.00. Earlier receipts are not known. Who can answer: Development. The Finance Lead decides.
4. Possible duplicate. GL-5118 and GL-5119: same date, account, description and amount (-860.50 each). Both are kept in the totals. Who can answer: the Bookkeeper. The Finance Lead decides.
5. Gift with no agreement reference. GL-5120, Gift, Donor D, 250.00. Who can answer: Development. The Finance Lead decides.
6. Account status "Confirm". GL-5122, Studio rent, October, account 6300, -1,800.00. Who can answer: the Bookkeeper. The Finance Lead decides.
7. Account status "Outside stated use". GL-5127, Flyers for open day, account 6400, -340.00. Who can answer: the Bookkeeper. The Finance Lead decides.
8. Account not in the coding table. GL-5136, Software subscription, account 7200, -65.00. Who can answer: the Bookkeeper. The Finance Lead decides.
9. Expense with a positive amount. GL-5140, Clay and paper order, refund, account 6200, +120.00. Who can answer: the Bookkeeper. The Finance Lead decides.
10. Transfer. GL-5142, 2026-10-28, -500.00, "per treasurer note". Who can answer: the Bookkeeper. The Finance Lead decides.

Rows left out of the totals: 2
GL-5116, 2026-10-14, 900.00: fund GEN, not SAF.
GL-5150, 2026-11-02, 300.00: dated after the period end.

Row check: 15 rows read = 13 placed in the schedule + 2 left out.

Draft for the Finance Lead's review. The finance lead confirms every classification, the permitted use and any entry. Nothing has been posted or changed.
```
