# Restricted gift rollforward

The finance lead gets a working schedule for one named restricted fund: opening balance, recorded gifts, coded expenditure and closing balance, with every unresolved difference listed from the gift agreement summary and the ledger detail. Nothing is posted.

*Workflow template · Nonprofits · Finance and accounting · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/restricted-gift-rollforward/)*

## The outcome

When someone asks what happened in a restricted fund this period, the finance lead has the answer on one schedule. It starts from the balance that was last reconciled, adds the gifts the ledger recorded, takes off the spending coded to the fund, shows any transfers, and ends at a closing balance that is compared with the ledger. Where the two do not agree, the schedule says by how much and which part of the gap comes from the opening balance and which from the movement.

The rest of the page is the work only a person can finish. Every gift with no agreement behind it, every expense on an account the fund coding does not cover, every possible duplicate and every transfer is listed with its reference, its amount and the person who can answer. The template does not decide what a fund may be spent on, and it reads no gift agreement itself: it works from a short summary of each agreement that the finance lead has already written.

## Who starts the work, and when

A bookkeeper or grants accountant starts it when finance needs to explain one restricted fund, usually at month end, before a funder report or when a program lead asks how much of a gift is left. The finance lead reviews the schedule, settles each listed difference and decides every classification and every entry. Development helps with gifts that arrive without an agreement reference.

## What they supply

- The fund, its code and the period.
- A summary of each gift agreement for the fund: reference, donor, the use as the finance lead states it, start and end dates and the amount stated.
- The fund coding the finance lead has approved, account by account.
- The ledger detail for the fund and period, as an export.
- The prior reconciled balance, and the ledger balances at the start and end of the period.

## What comes out

A working schedule in a fixed order: the stated uses as supplied, the rollforward with its difference, gifts by agreement, expenditure by the finance lead's coding, transfers, the numbered list of unresolved differences, the rows left out and a row count that proves every row in the export was placed or set aside.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Nonprofits](https://fullypowered.ai/industries/nonprofits/), where donors give for a stated purpose and the funder or board expects the books to show it.
- [Education](https://fullypowered.ai/industries/education/), for schools and foundations that hold endowed or program-restricted funds.
- [Healthcare](https://fullypowered.ai/industries/healthcare/), for community clinics and hospital foundations with gifts given for a named purpose.
- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which owns the ledger, the coding and the close.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), for organizations with a ledger and a routine already in place.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when restricted gifts multiply faster than one person can track them.

It is not [bank reconciliation preparation](https://fullypowered.ai/workflows/bank-reconciliation-preparation/), which matches a bank statement to the books, and it is not [journal entry preparation](https://fullypowered.ai/workflows/journal-entry-preparation/), which proposes entries. It proposes none.

## What has to change for your company

Keep a summary of each agreement, in your own terms, with the fund. Approve the fund coding account by account, with a status for each, and decide who may change it. Name who answers gift questions and who answers expense questions. Decide which entry types your ledger uses for gifts, expenses, transfers and adjustments, and how it signs amounts. Agree how often the schedule is prepared and where the prior reconciled balance is kept.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026; the record is published with it, lists the ambiguities it met, and lists the small edits made afterward that have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past period whose answer you already know, with cases written in advance: a gift with no agreement reference, a gift dated before its agreement began, an expense on an account missing from the coding, a possible duplicate and a ledger balance that does not agree. The finance lead checks every figure against the ledger before anything is relied on.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete workflow template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the workflow template drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related workflow templates

- [Bank reconciliation preparation](https://fullypowered.ai/workflow templates/bank-reconciliation-preparation/)
- [Journal entry preparation](https://fullypowered.ai/workflow templates/journal-entry-preparation/)
- [Month-end close checklist](https://fullypowered.ai/workflow templates/month-end-close-checklist/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
