# Restricted gift rollforward: tried once on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs are the invented example in `public/example.md` (Cedar Row Youth Arts, Studio Access Fund, October 2026). No client data was used. The run followed the fenced instruction block and the output format in `member/template.md`. The model that ran it did not write the template.

## Inputs used

The settings, the three-line agreement summary, the four-line fund coding, the fifteen ledger rows and the three balances in `public/example.md`, unchanged.

## What came out

The schedule below was produced from the inputs.

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
3. Gifts under AG-03 exceed the amount stated. GL-5112 (1,500.00) and GL-5133 (800.00) total 2,300.00 in this period; the summary states 2,000.00, an excess of 300.00. Earlier receipts are not known. Who can answer: Development. The Finance Lead decides.
4. Possible duplicate. GL-5118 and GL-5119: same date, account, description and amount (-860.50 each). Both are kept in the totals. Who can answer: the Bookkeeper. The Finance Lead decides.
5. Gift with no agreement reference. GL-5120, Gift, Donor D, 250.00. Who can answer: Development. The Finance Lead decides.
6. Account status "Confirm". GL-5122, Studio rent, October, account 6300, -1,800.00. Who can answer: the Bookkeeper. The Finance Lead decides.
7. Account status "Outside stated use". GL-5127, Flyers for open day, account 6400, -340.00. Who can answer: the Bookkeeper. The Finance Lead decides.
8. Account not in the coding table. GL-5136, Software subscription, account 7200, -65.00. Who can answer: the Bookkeeper. The Finance Lead decides.
9. Expense row with a positive amount. GL-5140, Clay and paper order, refund, account 6200, +120.00. Who can answer: the Bookkeeper. The Finance Lead decides.
10. Transfer. GL-5142, 2026-10-28, -500.00, "per treasurer note". Who can answer: the Bookkeeper. The Finance Lead decides.

Rows left out of the totals: 2
GL-5116, 2026-10-14, 900.00: fund GEN, not SAF.
GL-5150, 2026-11-02, 300.00: dated after the period end.

Row check: 15 rows read = 13 placed in the schedule + 2 left out.

Draft for the Finance Lead's review. The finance lead confirms every classification, the permitted use and any entry. Nothing has been posted or changed.
```

## What was observed

- Every part of the output format was produced, and nothing in the instructions required the run to stop. All headers matched, the fund and period were present, and the coding and balances were supplied.
- The arithmetic ties. The opening difference (+100.00) and the movement difference (+50.00) add to the total difference (+150.00). The row check ties at 15 = 13 + 2.
- A caveat on the comparison. The example file holds the inputs and the output together, and the whole file was read in one step before the run. So the run was not blind to the published output. The schedule above was worked out from the inputs, row by row, and the figures were recomputed rather than copied. A reader should still treat the close match with the example as weaker evidence than a blind run would give.
- Differences from the published example, all small:
  - Item 3. The example says the summary states 2,000.00, "300.00 less". The excess is 300.00 more than the amount stated, so the example's wording is wrong. The run says "an excess of 300.00".
  - Item 3. The example leaves out the sentence that earlier receipts are not known. Acceptance test 5 and the procedure ask for it, but the fenced instruction block does not mention it, so a run that follows only that block may leave it out too. The run added it from the procedure text.
  - Items 6 and 7. The wording is a little different ("Account status" rather than "Coding status is"). The format does not fix a wording for these.
  - Item 10. The example adds "The note was not supplied". The inputs only say "per treasurer note", so that sentence is an inference. The run left it out.
  - Item 4. The run wrote "kept in the totals" rather than "are in the totals". The meaning is the same.
- Facts in the outputs that are not in the inputs: only the "note was not supplied" sentence in the published example. The run added no other facts.
- Places where the instructions are open to more than one reading:
  - The order of the "rest" of the differences ("in the order of each item's lowest reference") is not defined for an item that covers several rows. The run used the lowest reference in each item, which gives the same order as the example. A different reading could give a different order.
  - The fenced block does not say what wording to use for a row left out. The longer procedure gives the reasons ("fund [code], not [code]", "dated after the period end"), but the block only lists the categories.
  - A positive-amount expense (GL-5140) is also a refund inside an account marked "Within stated use". It is counted in that account's total and listed as a difference. The instructions allow both, but do not say that the total for the account is the net.
  - The example does not exercise some paths: a missing coding table, a missing ledger balance, a gift whose agreement is for another fund, and a gift dated outside its agreement. These were not tried.
- Nothing in the run asked the model to stop, and nothing was posted, coded or changed.

## Edits made after the run

The recorded output and observations above are unchanged. After the run, the template and the published example were edited, and the template has not been run again. I checked the edited instruction block against the output format line by line and against the schedule above; the edits restate rules the run already followed from the procedure, so the same schedule is expected, but that is a check, not a new run.

- The instruction block now carries the earlier-receipts caveat, the repeated-reference duplicate, the stop on a summary that conflicts with itself, the wording of the left-out reasons, and the bookkeeper answering questions about balances.
- The output format now fixes a wording for each kind of difference, and step 6 says an account's total is net of a positive-amount refund.
- The published example now matches the schedule above in figures and facts, and uses the Kind wording fixed afterward (item 3 reads "Gifts above the amount stated." and item 9 "Expense with a positive amount." where the run wrote otherwise): "an excess of 300.00", the earlier-receipts sentence, "Account status" for items 6 and 7, "kept in the totals", and no sentence about the treasurer's note, which was an inference.
- After review, three more small edits, also not run again: the instruction block now says what to do when the coding is missing (every expenditure row goes under "Account not in the coding table") and that a blank end date means no end is stated; step 8 of the procedure says an item covering several rows is ordered by its lowest reference; and the description of the left-out row GL-5150 in the example's ledger was changed from Donor E to Donor C, since it carries Donor C's agreement reference. The run's output is unaffected by that description, which the schedule never prints.
