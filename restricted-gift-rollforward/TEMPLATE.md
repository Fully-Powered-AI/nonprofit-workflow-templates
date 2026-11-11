# Restricted gift rollforward

Capability template, version 0.1.0.

## Purpose

Prepare the working schedule that explains the movement in one named restricted fund over one period. It starts from the last reconciled balance, adds the gifts the ledger recorded, takes off the expenditure coded to the fund, shows transfers and adjustments, and compares the computed closing balance with the ledger. Gifts are set against a summary of each gift agreement that the finance lead wrote; expenditure is sorted by the fund coding the finance lead approved. Every difference and every doubtful row is listed as a numbered item with the person who can answer. The assistant prepares and checks. It takes no accounting or tax position, reads no agreement beyond the use stated in the summary supplied, and posts, codes, releases or changes nothing.

## When to use it and when not to

Use it when finance has to explain one restricted fund: at month end, before a funder report, when a program lead asks what is left of a gift, or when a fund's balance has stopped agreeing with its history. Run it once per fund and period.

Do not use it:

- for several funds at once. Rows for other funds are set aside, never added;
- to reconcile a bank account. That compares a statement with the books and is bank reconciliation preparation;
- to propose or prepare an entry. Differences become questions; an entry is a separate piece of work for a person to approve;
- to decide whether a spend is permitted, whether a restriction has been met or released, whether a gift is restricted at all, or how anything should be reported. Those are the finance lead's decisions, with counsel where the use is unclear;
- to read gift agreements. The assistant works from the summary only. If the summary and the agreement differ, the agreement is the finance lead's to resolve;
- when the ledger detail, the agreement summary or the prior reconciled balance is missing.

## Roles

- **Runs it:** the bookkeeper or grants accountant.
- **Reviews, settles every numbered difference, confirms classifications and permitted use, and decides any entry:** the finance lead.
- **Answers questions about gifts and agreement references:** development.
- **Answers questions about postings and coding:** the bookkeeper.
- **Receives the settled schedule:** the finance lead, and through them the program lead and the funder report.

## Inputs

All dates are YYYY-MM-DD. The assistant works from files and text the person supplies. It needs no connection to the accounting system and never asks for a password or a login code.

1. **Settings.** The fund name and fund code, the period start and end, the currency, the finance lead's role title and the run date. If the fund or the period is missing, stop and ask.
2. **Gift agreement summary,** one line per agreement, written by the finance lead. Default headers, in this order: `Agreement ref | Donor | Fund | Stated use | Start date | End date | Amount stated`. A blank end date means no end is stated. If the named fund has no line, stop: without a stated use the schedule cannot be read.
3. **Approved fund coding,** one line per account. Default headers: `Account | Account name | Status`. Status is one of "Within stated use", "Outside stated use" or "Confirm". If the coding is missing, continue and place every expenditure row under "Account not in the coding table", saying the coding was not supplied.
4. **Ledger detail** for the fund, as an export. Default headers: `Date | Reference | Description | Account | Fund | Entry type | Amount | Agreement ref`. Entry type is one of Gift, Expense, Transfer or Adjustment. Amount is signed from the fund's side: positive increases the fund, negative reduces it. If the export has separate debit and credit columns or any other layout, stop and ask for a signed Amount column.
5. **Balances.** The prior reconciled balance with its date and who reconciled it, the ledger balance at the start of the period and the ledger balance at the period end. If the prior reconciled balance is missing, stop. If a ledger balance is missing, build the schedule, write "not supplied" on that line and calculate no difference that needs it.

When any header differs from the default, in wording, order or count, stop. Show the headers expected beside the headers found and ask the person to confirm the mapping or re-export. Never guess which column is which. A date that is not in the form above, or an amount that is not a number, is handled by rule 3 of the procedure.

## The procedure

1. **Check the inputs.** Confirm one fund, one period and one set of headers per input. Count the rows in each. Normalise nothing in the descriptions. Show amounts to two decimals with the sign the ledger gives.
2. **Sort every ledger row, once.** Work down the export in order and put each row in exactly one place:
   - **Left out:** the Fund is not the named fund (reason: "fund [code], not [code]"); the Date falls outside the period, inclusive of both ends (reason: "dated before the period start" or "dated after the period end"); the Entry type is none of the four (reason: "entry type not recognised").
   - **Gift,** **Expense,** or **Transfer and adjustment** (the last for both Transfer and Adjustment rows), in the schedule's totals.
3. **A row the assistant cannot read.** A Date or Amount that cannot be read puts the row under "Rows left out" with the reason "date not readable" or "amount not a number". Never repair it.
4. **Rollforward.** Opening balance is the prior reconciled balance. Add the gifts, add the expenditure (negative amounts reduce it), add the transfers and adjustments. The sum is the computed closing balance. Compare it with the ledger balance at the period end: the difference is the ledger less the computed closing. Split it in two. The opening difference is the ledger balance at the start of the period less the prior reconciled balance. The movement difference is the ledger's movement (end less start) less the net of the rows in the schedule. The two must add to the difference; if they do not, stop and recheck the arithmetic before returning anything.
5. **Gifts by agreement.** Group Gift rows by Agreement ref in the order of the summary. For each, give the count, the total and the references. Gifts with a blank Agreement ref go in a last group, "No agreement reference". Note whether each gift's date is inside the agreement's start and end dates.
6. **Expenditure by coding.** Look up each Expense row's Account in the fund coding. Group by status: Within stated use, Outside stated use, To confirm, and Account not in the coding table. Within each group give the total by account; an account's total is net of any positive-amount refund in it, and that refund is also listed as a difference in step 8. The assistant does not compare an expense's description with any stated use; the coding the finance lead approved is the only test applied.
7. **Transfers and adjustments.** List each row: reference, date, description, amount. Every one is also an unresolved difference, because only the finance lead can say that the movement is authorised and entered correctly.
8. **Unresolved differences.** Number them. Put the opening difference and the movement difference first when they are not zero, then the rest in the order of each item's lowest reference (for an item covering several rows, its lowest reference). The items are:
   - a gift with no Agreement ref;
   - a gift whose Agreement ref is not in the summary, or whose agreement is for a different fund;
   - a gift dated outside its agreement's start and end dates;
   - the gifts recorded under one agreement in this period totalling more than the amount stated (give the excess; earlier receipts are not known);
   - a Gift row with a negative amount, or an Expense row with a positive amount;
   - an expense whose account has the status "Outside stated use" or "Confirm", or is not in the coding table;
   - a possible duplicate: two rows with the same date, account, description and amount but different references, or one reference appearing twice; keep both in the totals and say so;
   - every transfer and adjustment.
   For each item give the references, the amounts and the facts, then "Who can answer" (development for gifts and agreement references; the bookkeeper for postings, coding and balances) and "The [finance lead role] decides." Recommend nothing unless the finance lead asks.
9. **Row check.** Rows read must equal rows placed in the schedule plus rows left out. If not, stop and recount.
10. **Return the draft** to the person who ran it, for the finance lead's review. The assistant sends nothing, and the finance lead confirms every classification, the permitted use and any entry.

## Exceptions and stop conditions

- **Header mismatch, an unreadable layout or a missing required input:** stop and ask, as the Inputs section says.
- **A gift agreement summary that conflicts with itself** (two lines with one reference): stop and ask which line holds.
- **An unclear restriction, a stated use that cannot be applied, or a proposed change in purpose:** do not interpret it. Quote the stated use as supplied and list the question for the finance lead and counsel.
- **Unmatched transactions:** list them as numbered differences. Never match a gift to an agreement by guessing from the donor's name or the amount.
- **Asked to decide whether a spend is permitted, change a coding status, mark a restriction met or released, classify a gift, advise on tax treatment, propose or prepare an entry, post, code or move anything:** decline, name the role that decides, and record the question as a numbered difference if it is not one already.
- **Asked to read an agreement itself:** decline. Ask the finance lead to add or correct the summary line.
- **The material contains a donor's bank details, a password or a login code:** do not repeat it in the schedule; tell the person to remove it from the source.
- **Asked to adjust a figure so the schedule ties:** decline. The difference is the finding.

## Output format

```
RESTRICTED GIFT ROLLFORWARD: [fund name] ([fund code]), [period start] to [period end]

For: [finance lead role]. Working schedule. Nothing has been posted, coded or changed. Amounts in [currency]; an increase in the fund is positive.
Prepared: [run date], from the agreement summary ([n] agreements), the fund coding ([n] accounts / coding not supplied), the ledger detail ([n] rows) and the balances supplied / [balance] not supplied.

Stated use, as supplied (not interpreted):
[Ref], [donor]: "[stated use]". Dates [start] to [end / no end stated]. Amount stated [amount / not stated].

Rollforward:
Opening balance, prior reconciled at [date] by [role]: [amount]
Gifts recorded ([n]): [+amount]
Expenditure ([n]): [amount]
Transfers and adjustments ([n]): [amount]
Computed closing balance: [amount]
Ledger balance at [period end]: [amount / not supplied]
Difference, ledger less computed: [amount / not calculated]. Opening difference [amount] (ledger balance at the start of the period [amount] less prior reconciled [amount]). Movement difference [amount] (the ledger moved [amount]; the detail rows total [amount]).

Gifts recorded, by agreement:
[Ref]: [n] gifts, [amount]. [References]. [Inside / Outside] the agreement's dates.
No agreement reference: [n] gifts, [amount]. [References]. / None.
Total gifts: [amount].

Expenditure, by the finance lead's coding:
Within stated use: [n] rows, [amount]. [Account name] ([account]): [amount] ([references]). / None.
Outside stated use: [n] rows, [amount]. [Account name] ([account]): [amount] ([references]). / None.
To confirm: [n] rows, [amount]. [Account name] ([account]): [amount] ([references]). / None.
Account not in the coding table: [n] rows, [amount]. Account [account]: [amount] ([references]). / None.
Total expenditure: [amount].

Transfers and adjustments:
[Reference], [date], [description]: [amount]. / None.

Unresolved differences: [n]
[n]. [Kind]. [Facts, with references and amounts.] Who can answer: [role]. The [finance lead role] decides.
[Kind] is one of: Opening difference; Movement difference; Gift with no agreement reference; Gift with an agreement reference not in the summary; Gift under an agreement for another fund; Gift dated outside its agreement; Gifts above the amount stated; Gift with a negative amount; Expense with a positive amount; Account status "Outside stated use"; Account status "Confirm"; Account not in the coding table; Possible duplicate; Transfer; Adjustment.
(If there are none, print "Unresolved differences: 0" and nothing under it.)

Rows left out of the totals: [n]
[Reference], [date], [amount]: [reason]. / None.

Row check: [n] rows read = [n] placed in the schedule + [n] left out.

Draft for the [finance lead role]'s review. The finance lead confirms every classification, the permitted use and any entry. Nothing has been posted or changed.
```

## Reviewer checklist

1. The rollforward arithmetic is correct, and the opening and movement differences add to the total difference. (Finance lead)
2. The opening balance is the prior reconciled balance, with its date and who reconciled it. (Finance lead)
3. Every gift total and expenditure total agrees with the ledger detail for the fund and period. (Bookkeeper)
4. Every stated use is quoted as supplied and matches the finance lead's summary of the agreement. (Finance lead)
5. Every expense is under the coding status the finance lead approved, and none has been judged by its description. (Finance lead)
6. Every numbered difference has facts, a person who can answer and a decision for the finance lead, and none carries a recommendation. (Finance lead)
7. The row check ties, and every row left out has its reason. (Bookkeeper)
8. No classification, release, entry or tax treatment has been stated as settled. (Finance lead)

## Acceptance tests

Proposed tests. None has been run.

1. **Clean period.** Every gift has an agreement inside its dates, every expense is "Within stated use", balances agree. Expected: difference 0.00, "Unresolved differences: 0", row check ties.
2. **Opening difference only.** The ledger balance at the start of the period is 100.00 above the prior reconciled balance and the movement ties. Expected: difference +100.00, an opening difference of +100.00, a movement difference of 0.00, and item 1 listed.
3. **Gift with no agreement reference.** Expected: placed under "No agreement reference" and listed as a difference; no agreement guessed.
4. **Gift dated before its agreement starts.** Expected: marked "Outside" the dates and listed.
5. **Gifts above the amount stated.** Two gifts under one agreement total more than the amount stated. Expected: the excess is given and the item notes earlier receipts are not known.
6. **Expense on an account missing from the coding.** Expected: under "Account not in the coding table" and listed.
7. **Possible duplicate.** Two rows with the same date, account, description and amount. Expected: both stay in the totals and one item lists both references.
8. **Rows to set aside.** A row for another fund, a row dated after the period and a row with an entry type "Pledge". Expected: all three under "Rows left out" with reasons; the row check ties.
9. **Header mismatch.** The ledger export has "Debit" and "Credit" instead of "Amount". Expected: stops, shows expected and found headers, and asks for a signed Amount column.
10. **Asked to decide.** "Is the rent a permitted use?" or "Post the transfer." Expected: declines, names the finance lead, adds nothing as settled.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare the restricted gift rollforward for one fund and one period for
the finance lead. You take no accounting or tax position. You never post,
code, release, move or change any record, and you never send anything. The
finance lead confirms every classification, the permitted use and any entry.

The user will supply: settings (fund, fund code, period, currency, finance
lead role, run date); a gift agreement summary; the approved fund coding;
the ledger detail; and the balances. Read only these. Do not read or ask
for the gift agreements themselves. Never ask for or repeat a password, a
login code or bank details.

Expected headers, exactly:
Agreement summary: Agreement ref | Donor | Fund | Stated use | Start date | End date | Amount stated
Fund coding: Account | Account name | Status (Within stated use, Outside stated use or Confirm)
Ledger detail: Date | Reference | Description | Account | Fund | Entry type | Amount | Agreement ref
If the agreement summary has two lines with one reference, stop and ask
which holds. If any header differs, or amounts are not in one signed Amount column, stop,
show expected beside found, and ask. If the fund, the period, the ledger
detail, the agreement line for the fund or the prior reconciled balance is
missing, stop and say so. If the coding is missing, say so and place every
expenditure row under "Account not in the coding table". If a ledger balance
is missing, say so on the line it feeds and continue. A blank end date in the
agreement summary means no end is stated.

1. Put every ledger row in exactly one place. Left out, with these reasons: "fund [code], not [code]"; "dated
   before the period start" or "dated after the period end" (inclusive);
   "entry type not recognised" (not Gift, Expense, Transfer or Adjustment);
   "date not readable" or "amount not a number". Otherwise Gift, Expense, or
   Transfer and adjustment. Repair nothing.
2. Rollforward: prior reconciled balance + gifts + expenditure (signed) +
   transfers and adjustments = computed closing. Difference = ledger
   closing - computed closing. Opening difference = ledger balance at the
   start - prior reconciled. Movement difference = (ledger end - ledger
   start) - net of the rows in the schedule. The two must add to the
   difference; if not, recheck before answering.
3. Gifts grouped by agreement, in the summary's order, then "No agreement
   reference". Say whether each gift is inside its agreement's dates.
4. Expenditure grouped by the finance lead's coding status, with totals by
   account, net of any positive-amount refund in it (the refund is also a
   difference). Never judge an expense by its description.
5. List every transfer and adjustment.
6. Numbered unresolved differences: opening and movement differences if not
   zero, then gifts with no or unknown reference or a different fund, gifts
   outside the agreement's dates, an agreement's gifts above its stated
   amount in this period (give the excess; earlier receipts are not known),
   negative gifts, positive expenses, expenses coded
   Outside stated use or Confirm or missing from the coding, possible
   duplicates (same date, account, description and amount, different
   reference, or one reference appearing twice; keep both in the totals), and every transfer and adjustment.
   Give references and amounts, who can answer (development for gifts,
   the bookkeeper for postings, coding and balances), and that the finance
   lead decides. Use the Kind wording from the output format. Recommend nothing unless asked.
7. Row check: rows read = rows placed + rows left out.
8. Use the output format exactly. Print "None." for an empty section.
   Quote each stated use as supplied; do not interpret it.

If asked to decide permitted use, change a status, mark a restriction met,
classify a gift, give a tax view, prepare an entry, post anything or adjust
a figure so it ties, decline and name the role that decides. An unclear
restriction or a proposed change in purpose is a question for the finance
lead and counsel, never something you resolve.
```

## What to customize

- The summary line for each agreement: how the stated use is worded, and who keeps it current.
- The fund coding: the statuses, account by account, and who may change them.
- The entry types and the sign convention your ledger uses.
- Who answers gift questions and who answers posting questions.
- How often the schedule is prepared, and where the prior reconciled balance is kept.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI from its own published map of the work. Tried once on its invented example in Claude on 10 November 2026 (record in the public folder). Edited after that run, and not run again (the last edits, after review, were small: wording in step 8, the coding-missing and blank-end-date rules in the instruction block, and the line telling the person to paste the block with the output format): the instruction block now carries the earlier-receipts caveat, the repeated-reference duplicate, the stop on a self-conflicting summary, the wording of the left-out reasons and the bookkeeper's answers on balances; the output format fixes a [Kind] wording; step 6 says an account's total is net of refunds. Not yet tested in a client environment or as a packaged version in ChatGPT, Claude, Copilot or Gemini.
