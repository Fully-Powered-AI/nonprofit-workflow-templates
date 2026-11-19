# AI workflow templates for nonprofit staff

FullyPowered Workflow Templates for nonprofit organizations turn the AI your organization already pays for into a team that knows how the work is done: a donor services team with a thank-you drafted for every new gift, a grants manager with the funder report drafted to the funder's own questions, a finance lead with one restricted fund rolled forward and every difference listed. 6 workflow templates, made to be customized and deployed. All plain Markdown, all free, MIT license.

We are FullyPowered AI. We build AI workflows for companies, and these are the templates we start from. We publish them because a good starting point should be open to everyone. Copy one. Change it. Make it yours.

> [!TIP]
> **Missing a template that is not listed here, or want these customized for your organization? Reach out to us.** These are templates, made to be customized and deployed. FullyPowered AI customizes and builds AI workflows, connects them to your business systems, installs them in your agents and puts them in the hands of the people who own the work. [See more examples for nonprofit organizations](https://fullypowered.ai/industries/nonprofits/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-readme&from=gh-nonprofit-readme) · [Have one built for your team](https://fullypowered.ai/pricing/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-readme&from=gh-nonprofit-readme) Not sure where to start? Email hello@fullypowered.ai and a person will answer.

**Who this is for**

- Executive directors and board chairs who have paid for AI and want it doing real work.
- Development, program and finance leads who want something their team can run this week.
- The staff member who does the work, who gets a precise way to prepare it and still makes the call.

**What these are for**

- **Your best way of doing it, for the whole team.** One piece of work, written down precisely enough that an assistant prepares it the same way every time.
- **Work you can check.** Every template says what it needs, what it produces, what it checked and what it could not.
- **A person decides.** Anything that sends, posts, pays or changes a record waits for someone to approve it.
- **Tied into your business systems.** A workflow can be designed to pull from the systems your company already runs, and even push data back into them, with guardrails and a person approving. [Browse the Connectors Directory](https://fullypowered.ai/connectors/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-readme&from=gh-nonprofit-readme).
- **Free, open and portable.** MIT-licensed plain instructions that run in the assistant or agent your team already uses: ChatGPT, Claude, Claude Code, Claude Cowork, Codex, Copilot, Gemini, Grok, Perplexity.

**Quick start**

1. **Draft thank-yous for your latest gifts.** Open ChatGPT, Claude, Copilot or Gemini. Copy the text below into a new chat. Replace the square-bracket parts with a short list of recent gifts, your donors' preferences and the lines your team has approved for describing each program. Use invented or trimmed data if you prefer.

   ```text
   You draft donor thank-you messages for a person on our donor services team. Never send anything, never write a tax receipt or tax statement, never ask for another gift, and never change a record. A person reads and sends every message.

   Here are my inputs. Gifts: [gift ID, date, donor, amount, fund, anonymous yes or no, status]. Donor preferences: [preferred name, channel, whether to mention the amount, do not contact]. Approved program language: [one line per program, with its review date]. Signer: [name and title]. Word limit: [number].

   Write one short draft for each confirmed gift, using only the approved program lines. Set aside anonymous gifts, disputed gifts and do-not-contact donors, with the reason and who decides. Add a note for the sender on anything odd, such as a tax question. Finish by checking that every gift is either drafted or set aside.
   ```

2. Read what comes back. It marks what it checked and what is left for you. What comes back, with invented data:

   ```text
   DONOR THANK-YOU DRAFTS: Harbor Lane Food Pantry
   Status: Drafts for Marcus Ibarra, Donor Services. Nothing has been sent.
   Run date: Monday 9 November 2026. Register rows: 8. Drafts: 6. Set aside: 2.
   Program language: P1, P2 and P3 used; G1 current, not needed (every fund has a line). All inside the 365-day review period.
   Finance receipt line: none supplied, so no receipt wording appears anywhere.

   DRAFTS

   1. G-2041, Tessa Brandt (D-118). Email. Program line: P1.
   Subject: Thank you for your gift
   ```

3. Stop there. You will know if this is for you. When you want it fitted to your company, or built into your agents, [that is what we do](https://fullypowered.ai/pricing/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-readme&from=gh-nonprofit-readme).

In every workflow a person starts the work, supplies the inputs and decides; the template prepares and checks, and none of them decides who gets help or takes a tax or legal position.

These are samples and a starting point, made to be changed to fit how your organization works. The work you do may not be here, and we can build a workflow for it, whether it takes one step or many.

## The workflow templates here today

- **[Board minutes draft](board-minutes-draft/)**: After a board meeting, the secretary gets draft minutes built only from what they supply: notes, agenda, motion text and vote record. Attendance, motions, votes, documents and actions are laid out, and every gap is marked for the secretary to settle.
- **[Donor thank-you drafts](donor-thank-you-drafts/)**: Donor services staff get one draft thank-you for each new gift, written from the confirmed gift details, the donor's communication preferences and the organization's approved program language. A person checks and sends every message; nothing asks for another gift.
- **[Funder report draft](funder-report-draft/)**: Before a funder report is due, the grants manager gets a draft written to the funder's own questions, with every number tied to a record, an index of the evidence behind each statement and a list of what is still unanswered. People verify it, approve it and submit it.
- **[Program outcome map](program-outcome-map/)**: Before an evaluation, the program and evaluation leads get one map linking each activity to the outcome it is meant to serve, with proposed measures, data sources, assumptions and the questions the evidence cannot yet answer. It claims no impact.
- **[Restricted gift rollforward](restricted-gift-rollforward/)**: The finance lead gets a working schedule for one named restricted fund: opening balance, recorded gifts, coded expenditure and closing balance, with every unresolved difference listed from the gift agreement summary and the ledger detail. Nothing is posted.
- **[Volunteer shift options](volunteer-shift-options/)**: A volunteer lead gets draft shift options once an event's availability replies are in: each role's needs set against who volunteered, the requirements on record and the shifts already confirmed, with every uncovered position shown. The lead checks and confirms; nothing is assigned or sent.

## How to use one

Open a folder and start with its README. Every folder stands alone, so copy the one you want and leave the rest. The templates are written for ChatGPT, Claude, Copilot and Gemini: paste the instruction block and the output format in as custom instructions, or load the folder in a product that reads `SKILL.md` packages.

To take the whole collection, press **Use this template** at the top of this page: it copies every folder into a repository in your own account, yours to change.

In every template a person starts the work, supplies the inputs and decides. The template prepares and checks. Anything that sends, posts, pays or changes a record waits for a person to approve it.

## What SKILL.md is

Each folder holds a file named `SKILL.md`. It is the technical file: the same instructions and output format as the template, in the packaged form that AI products which load instructions from a folder read. It is generated from `TEMPLATE.md`, so the two always agree. The workflow template is the whole folder; `SKILL.md` is one way of loading it. If your AI product does not read that format, use `TEMPLATE.md`.

## What "checked" means here

Each folder says exactly what was checked and when: who wrote it, that its sources and rights were reviewed, the date of its editorial review, and whether it has been tried on its invented example in a named AI product. Nothing is described as tested for a client unless it was. Test a template on your own past work before your team relies on it; each one comes with acceptance tests for that.

## More workflow templates

The [FullyPowered Workflows Directory](https://fullypowered.ai/workflows/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-readme&from=gh-nonprofit-readme) lists every workflow template across functions and industries, with search. A machine-readable list of this repository is in [index.json](index.json).

For the work these templates come from, by area of the business and by task, see [AI workflow examples for nonprofits](https://fullypowered.ai/industries/nonprofits/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-readme&from=gh-nonprofit-readme).

## Licence and credits

MIT, in [LICENSE](LICENSE) and in every folder. Each folder's SOURCES.md names what the workflow template drew on. Published by [FullyPowered AI](https://fullypowered.ai/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=nonprofit-readme&from=gh-nonprofit-readme).
