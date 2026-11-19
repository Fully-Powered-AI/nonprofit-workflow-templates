# Membership renewal and lapse list

A monthly list from your member export: who is due to renew, who is in the grace period and who has lapsed, with drafts per level for a person to send.

> [!TIP]
> **Missing a template that is not listed here, or want these customized for your organization? Reach out to us.** This is a template, made to be customized and deployed. FullyPowered AI customizes and builds AI workflows, connects them to your business systems, installs them in your agents and puts them in the hands of the people who own the work. [See Membership renewal and lapse list on our website](https://fullypowered.ai/workflows/membership-renewal-and-lapse-list/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-membership-renewal-and-lapse-list&from=gh-membership-renewal-and-lapse-list). Not sure where to start? Email hello@fullypowered.ai and a person will answer.

**Quick start**

1. Read EXAMPLE.md to see what a good result looks like.
2. Copy all of TEMPLATE.md into your assistant, then give it your own inputs, or the invented ones from EXAMPLE.md.
3. Read what comes back. It marks what it checked and what is left for you.

*Workflow template · Nonprofits · Customer success and account management · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/membership-renewal-and-lapse-list/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-membership-renewal-and-lapse-list&from=gh-membership-renewal-and-lapse-list)*

## The outcome

Renewals stop slipping through the gaps between a spreadsheet and a busy month. On the day the coordinator sits down to do renewals, the whole membership is sorted on one page: the people whose renewal date falls inside your reminder window, with those on automatic renewal shown apart, the people past their renewal date but still inside your grace period, and the people who have lapsed since the list was last made. The size of every group is shown, and a totals line ties them to the rows you exported, so nobody falls off the page unnoticed.

The records that would cause a wrong message are caught first: a renewal date that is blank or could not exist, a payment recorded after the renewal date that never moved, a member marked lapsed whose renewal is still ahead. Those come out as a short list to fix, with no draft attached.

For each membership level there is a renewal reminder and a lapsed-member note, ready to merge, written only from the facts your organization has approved: the fee, what membership includes, how to renew or rejoin and where to ask. Every member at a level gets the same wording. Nobody is ranked, singled out or judged on what they might pay or give.

The coordinator stays in charge. The workflow template sends nothing, takes no payment, changes no status and cancels nobody. It honors each member's contact preference and never drafts for anyone marked do not contact.

## Who starts the work, and when

The membership coordinator or membership administrator starts it once a month, on the day renewals are done, after taking a fresh export from the membership system. The coordinator reads the list, fixes the records it flags in the system, edits the drafts and sends them to the right people. Where your rules name someone else to sign a level's notes, such as a chair, that person approves those notes. The membership lead owns the approved facts the drafts are built from.

## What they supply

- **The member export from your membership management system**, with these columns: member_id, name, membership_level, joined_at, renewal_date, status (active, lapsed or cancelled), auto_renew (yes or no), last_payment_at, contact_preference (email, post or phone) and do_not_contact (yes or no). If your system names a column differently, the workflow template stops and asks which column is which.
- **Your renewal rules:** how many days ahead a reminder goes, how long the grace period runs before a member counts as lapsed, who signs reminders and lapsed notes at each level, the subject line each carries, your organization's name and the date the list was last made.
- **Your approved facts for each level:** the fee for the year, what membership includes, how to renew, how to rejoin, where to ask questions and any welcome-back line, each written as the sentence you want members to read.
- **Today's date.**

## What comes out

One list in a fixed order. A totals line that proves every row of the export is in exactly one group. Then the groups: due to renew with a reminder, due to renew on automatic renewal, in the grace period with the date each membership stays open until, lapsed since the last run, and records to check with the field and the problem named. A section on who was left out and why: anyone marked do not contact, cancelled members, and members who lapsed before the last run and were listed then. Then the draft renewal reminders and lapsed-member notes, one per level, each with the members it is for and who signs it. Where a group is empty, the list says "None."

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Customer success and account management](https://fullypowered.ai/functions/customer-success-and-account-management/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-membership-renewal-and-lapse-list&from=gh-membership-renewal-and-lapse-list), because keeping members is keeping the people who already chose you.
- [Nonprofits](https://fullypowered.ai/industries/nonprofits/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-membership-renewal-and-lapse-list&from=gh-membership-renewal-and-lapse-list), where associations and member-funded organizations depend on renewals arriving every year.
- [Education](https://fullypowered.ai/industries/education/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-membership-renewal-and-lapse-list&from=gh-membership-renewal-and-lapse-list), for alumni associations, parent groups and learned societies that run on annual membership.
- [Hospitality](https://fullypowered.ai/industries/hospitality/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-membership-renewal-and-lapse-list&from=gh-membership-renewal-and-lapse-list), for clubs whose members renew each season and expect a word before their membership runs out.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-membership-renewal-and-lapse-list&from=gh-membership-renewal-and-lapse-list), for organizations with a long member list and a renewal routine that lives in one person's head.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-membership-renewal-and-lapse-list&from=gh-membership-renewal-and-lapse-list), when the member list grows faster than one coordinator can check by hand.

It is not [donor thank-you drafts](https://fullypowered.ai/workflows/donor-thank-you-drafts/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-membership-renewal-and-lapse-list&from=gh-membership-renewal-and-lapse-list), which thanks a gift, and it is not [renewal risk review](https://fullypowered.ai/workflows/renewal-risk-review/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-membership-renewal-and-lapse-list&from=gh-membership-renewal-and-lapse-list), which looks at a business's customer accounts coming up for renewal. [Lapsed customer win-back](https://fullypowered.ai/workflows/lapsed-customer-win-back/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-membership-renewal-and-lapse-list&from=gh-membership-renewal-and-lapse-list) works with customers who have stopped buying; this one works with members and your own renewal rules.

## What has to change for your company

Set your reminder window and grace period, and the day of the month you make the list. Match the column names to your membership system's export. Write the approved sentences for each level, with someone who owns them and keeps them current. Decide who signs reminders and lapsed notes at each level. Decide whether members on automatic renewal should hear from you in advance; by default they get no reminder. Agree who fixes the records the list flags. The workflow template reads the export you supply and needs no connection to your membership system, so it runs in ChatGPT, Claude, Copilot or Gemini.

## What has been checked

FullyPowered AI wrote this workflow template. It was editorially reviewed on 19 November 2026. It was tried on its invented example on 19 November 2026, and the record is published with it. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past month whose renewals you already know, with cases written in advance: a renewal date that could not exist, a payment after a renewal date that did not move, a member marked do not contact, a member on automatic renewal whose date has passed, and a renamed column. The coordinator checks the totals line and three rows by hand before anything is sent.

- Written by FullyPowered AI.
- Sources and rights reviewed.
- Editorially reviewed on 19 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 19 November 2026. The record is in [TRIAL.md](TRIAL.md).
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

- [Donor thank-you drafts](../donor-thank-you-drafts/)
- [Renewal risk review](https://fullypowered.ai/workflows/renewal-risk-review/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-membership-renewal-and-lapse-list&from=gh-membership-renewal-and-lapse-list)
- [Lapsed-customer win-back](https://fullypowered.ai/workflows/lapsed-customer-win-back/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-membership-renewal-and-lapse-list&from=gh-membership-renewal-and-lapse-list)

## Make it yours

This workflow template is an example and a starting point. FullyPowered AI adapts it to how your company works, proves it on real work and rolls it out to the roles that use it. We can also build any other workflow for your company, including one that runs several steps, in a Workflow Sprint or a scoped implementation. [Talk with us](https://fullypowered.ai/contact/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-membership-renewal-and-lapse-list&from=gh-membership-renewal-and-lapse-list).
