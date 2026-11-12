# Volunteer shift options

A volunteer lead gets draft shift options once an event's availability replies are in: each role's needs set against who volunteered, the requirements on record and the shifts already confirmed, with every uncovered position shown. The lead checks and confirms; nothing is assigned or sent.

*Workflow template · Nonprofits · People and HR · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/volunteer-shift-options/)*

## The outcome

The replies are in and the lead can see the whole event on one page. For every shift and role, the page shows how many places are needed, how many are already confirmed, how many are waiting on an answer, and which volunteers could take what is left. Two draft options follow, one that fills places in a set order until no more can be filled (not a guaranteed maximum) and one that gives each volunteer a single shift, so the lead can see what each choice costs in gaps.

The gaps are never hidden. A place nobody can take is shown as uncovered, with the reason. A volunteer whose requirement is not on record is shown as a possibility to check, never as cover. Interest is not qualification, and a pending confirmation is not a confirmation.

The lead still decides. The template rates, ranks and turns away no one, places nobody for good and contacts no volunteer. Suitability, assignments and every conversation with a volunteer stay with the lead.

## Who starts the work, and when

The volunteer lead starts it when the availability replies for an event have come in and some places on the role list are still open. It runs again when a late reply arrives, when someone withdraws or when the role list changes. The lead reviews both options, adjusts them and confirms assignments with volunteers directly. Event staff and program delivery read the result once the lead has settled it.

## What they supply

- The event's role list: for each shift, its date and hours, each role, how many places are needed and any requirement for the role.
- The availability replies: for each volunteer, the date, the hours they offered, the roles they chose, the most shifts they will do and any note they wrote.
- The qualification records you already keep, such as a food handler card or a completed training, with each record's status and expiry.
- The assignments already made, confirmed or still pending.
- A few settings: the event name, today's date and a default limit on shifts per volunteer.

## What comes out

One page in a fixed order. The places still to fill, with the volunteers who could take each. Two draft options, each showing who is placed where, what is left uncovered and why, and which volunteers are not placed. Then the flags that need a person: pending confirmations, hours that do not cover a shift, requirements not on record, volunteers' own notes, and questions only the lead can settle. Volunteers appear by the code and name in your files, and no contact details are repeated.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [People and HR](https://fullypowered.ai/functions/people-and-hr/), because the work is matching people to places, with the lead keeping every decision about them.
- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), where an event's day is made to work with the people who offered.
- [Nonprofits](https://fullypowered.ai/industries/nonprofits/), where events run on volunteers and the replies arrive in a pile.
- [Education](https://fullypowered.ai/industries/education/), for school and college events staffed by parents, alumni and students.
- [Government](https://fullypowered.ai/industries/government/), for community events run by a public office or library.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), for organizations that hold the same events year after year.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when the volunteer list outgrows what a lead can hold in their head.

It is not the [event plan](https://fullypowered.ai/workflows/event-plan/), which plans the event itself, and it is not the [employee onboarding plan](https://fullypowered.ai/workflows/employee-onboarding-plan/), which welcomes someone who has already joined. The [service roster options](https://fullypowered.ai/workflows/service-roster-options/) work in headcounts for paid staff; this one works with named volunteers and the offers they made.

## What has to change for your company

Rename the roles and shifts to match your events. List the requirements you actually set and where each is recorded. Decide your default limit on shifts per volunteer and whether a volunteer may work two shifts that touch. Decide who confirms assignments and in what words, since the template writes no message to volunteers. Agree how late replies and withdrawals reach the lead. Keep contact details out of what you paste. The template reads files you supply and needs no connection to your volunteer database, so it runs in the AI product your team already uses.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried once on its invented example in Claude on 10 November 2026; the record of that run is published with it. Edits made after that run have not been run again: Option 1 was renamed, its overlap rule now also excludes a volunteer whose drafted shifts overlap, the date style and the rules for "Limit not stated for", "limit reached" and shared questions were settled, and the example was corrected to match. Its acceptance tests 2 to 14 are proposed and have not been run. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past event whose staffing you already know, with cases written in advance: a reply that covers only part of a shift, an expired card, a volunteer with a note about back-to-back shifts, a pending confirmation and a renamed column. The lead checks every place against the files before anyone is asked to confirm.

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

- [Event plan](https://fullypowered.ai/workflow templates/event-plan/)
- [Employee onboarding plan](https://fullypowered.ai/workflow templates/employee-onboarding-plan/)
- [Service roster options](https://fullypowered.ai/workflow templates/service-roster-options/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
