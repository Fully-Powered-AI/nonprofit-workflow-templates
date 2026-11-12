# Donor thank-you drafts

Workflow template, version 0.1.0.

## Purpose

Draft one thank-you for each newly confirmed gift in a batch, using only the gift details in the register, the donor's communication preferences and the organization's approved program language. Every draft names its channel and the approved line it used. Gifts that need a person's judgment are set aside with the reason and the role that decides. The assistant prepares; it never sends a message, never writes a tax receipt or tax statement, never asks for anything, and never changes a record.

## When to use it and when not to

Use it after a batch of gifts has been confirmed in the gift register: the day they are posted, or at the end of the week.

Do not use it:

- to write a tax receipt, a tax statement or any wording about deductibility. Finance owns those, and they come from the giving system;
- to ask for another gift, renew a pledge or invite anyone to an event. Those are separate pieces of work with their own approvals;
- to answer a message a donor has sent. Use customer reply drafting for a reply to a message that has arrived;
- to open a conversation with someone new. Use creator outreach drafting for first contact;
- when the register has no status column, because the assistant cannot tell a confirmed gift from a pending one.

## Roles

- **Runs it:** a donor services staff member.
- **Reads, edits, approves and sends every message:** donor services.
- **Decides anonymous gifts, and any gift whose donor asked not to be contacted:** the donor services lead.
- **Reviews receipt wording, disputed amounts, tax questions and the value of donated goods:** finance.
- **Owns and reviews the approved program language:** the development director, or whoever the organization names.

## Inputs

1. **The gift register export.** One row per gift. Default column headers: Gift ID, Gift date, Donor ID, Donor name, Amount, Gift type, Fund, Anonymous, Status, Notes. If a header does not match, stop and ask which of the supplied columns stands for it; never guess. Notes may be empty. Amount may be empty only for an in-kind gift.
2. **Donor preferences.** One row per donor. Default headers: Donor ID, Preferred name, Channel, Mention amount, Do not contact. If a donor has no row, use the name in the register, the channel Email and no mention of the amount, and say so on that draft. If the Do not contact column is missing, stop and ask.
3. **Approved program language.** Short numbered lines, each with a fund or "General" or "Tribute gifts", the date it was last reviewed and its owner. If none is supplied, stop. If a fund has no line, use the General line; if there is none, leave the program sentence out and say so.
4. **The settings.** The organization's name, who signs and with what title, the run date, the thank-you window in business days, the length limit in words, the review period for program language in days, the currency, any receipt line finance has approved, and the amount rule. If a setting is missing, use the default named in the procedure (currency: USD) and say so. If the signer is missing, stop.

The assistant works from files and notes the person supplies. It needs no connection to the giving system or the mail system and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Confirm the headers. Count the register rows. If a Gift ID appears twice, stop and ask which row is right; do not draft either.
2. **Check the program language.** A line is current if its review date is within the review period (default 365 days) of the run date. Use only current lines. If a line is not current, treat the fund as having no line and say which line was passed over.
3. **Sort each row.** Work down the register in order and place every row in exactly one place:
   - Status is not Confirmed (Pending, Disputed, anything else): set aside, reason "status is [status]", decided by finance.
   - Anonymous is Yes, or is blank: set aside, reason "anonymous" or "anonymity not stated", decided by the donor services lead. Do not draft under any name.
   - The donor's Do not contact is Yes: set aside, reason "do not contact", decided by the donor services lead.
   - Anything else is drafted.
4. **Set the channel, the greeting and the closing.** Use the donor's Channel (Email, Letter or Card). Greet "Dear [Preferred name]," or, if there is none, "Dear [register name],". Do not shorten or invent a name. If the name as given does not read after "Dear" (for example it begins with "the"), greet "To [name]," and note it for the sender. Unless the organization has set its own, the sign-off is "With gratitude," and an Email's subject is "Thank you for your gift".
5. **State the gift.** Write "Thank you for your gift of [amount] for the [Fund], received on [day month]." Write the amount with the currency from the settings (default USD, written with the "$" sign) and the figure as the register gives it. Name the amount only if the Mention amount preference is Yes, or the amount rule (default: name the amount of a confirmed cash gift unless the preference is No) says to; otherwise leave out "of [amount]". Never name an amount for an in-kind gift and never state a value for donated goods; write "Thank you for the [what was donated, as the Notes give it] you donated for the [Fund], received on [day month]." A first gift of a monthly series is written "Thank you for starting a monthly gift for the [Fund]; your first gift was received on [day month]." and the yearly total is not worked out. A further gift from a donor who is thanked earlier in the same batch is drafted as usual with "your further gift", and flagged in both notes for donor services to decide whether to combine.
6. **Add one approved program sentence** (for a tribute gift, the Tribute line then the fund line). Use the line for the gift's fund, word for word. Do not change it, shorten it or add any figure, result or story it does not contain. A tribute gift uses the Tribute line with the honoree named exactly as the Notes give, then the fund line; the gift sentence itself does not name the honoree, so the name appears once. If the Notes name an honoree and no Tribute line is supplied, leave the tribute sentence out, do not name the honoree anywhere, and flag it.
7. **Add nothing else.** No request for a gift, a pledge, a renewal, an event, a survey or a link. No mention of an outstanding balance. No receipt, tax or deductibility wording. If finance has supplied an approved receipt line, place it unchanged after the program sentence and mark it "finance-approved wording"; otherwise write none.
8. **Route questions.** If the Notes raise tax treatment, deductibility, a receipt or the value of donated goods, draft the thanks without touching the question and note "send to finance". If the Notes say the donor is giving in someone's memory or honor, do not draft any notice to the family or the honoree.
9. **Check the timing.** Count business days (Monday to Friday) after the gift date up to and including the run date. If the count is greater than the window (default 4), flag the draft "past the window" with the count. Do not add an apology or any reference to delay in the text.
10. **Check the length.** Count words from the greeting through the signature. If the count is over the limit (default 110), shorten the gift sentence, never the approved line, and count again.
11. **Close the batch.** Count rows: drafted plus set aside must equal register rows. List the Gift IDs in each group. List the word count of each draft.

## Exceptions and stop conditions

- **A header does not match, the signer is missing, or no program language is supplied:** stop and ask.
- **A Gift ID appears twice:** stop on that ID.
- **Row counts do not add up:** stop and report the figures.
- **An amount is present but not a number, or a gift date is not a date:** set the row aside as "unreadable [field]", decided by donor services.
- **Asked to write a receipt or tax statement, state a deductible amount, value donated goods, add an ask, or send a message:** decline. The first three belong to finance, and sending belongs to donor services.
- **Asked to invent program detail, a result or a story:** decline. Only approved lines are used.

## Output format

```
DONOR THANK-YOU DRAFTS: [Organization]
Status: Drafts for [signer]. Nothing has been sent.
Run date: [day date]. Register rows: [n]. Drafts: [n]. Set aside: [n].
Program language: [lines used, each current or passed over, with the reason].
Finance receipt line: [supplied, placed unchanged, or none supplied, so no receipt wording appears anywhere].

DRAFTS

[n]. [Gift ID], [donor name] ([Donor ID]). [Channel]. Program line: [IDs].
[Subject: ... for Email only]

[Greeting],

[Draft text]

[Sign-off]
[Signer]
[Title, Organization]

Note for the sender: [past the window with the count; amount not named and why; combine decision; send to finance; any default used]. [Write "none" if there is nothing.]

[Repeat for each draft. If there are none, write "None."]

SET ASIDE

- [Gift ID], [description] ([Donor ID]), [gift date]. [Reason]. [Role that decides].
[If nothing is set aside, write "None."]

CHECK

Register rows [n] = drafts [n] + set aside [n]. Gift IDs drafted: [list]; set aside: [list]. Word counts, greeting through signature: [item, count] ...; limit [n].
Asks: [none of the drafts asks for a gift, a pledge, an event or a click, or name each exception]. Tax and receipt wording: [none in any draft, or the finance-approved line placed unchanged].

Prepared for [signer]. Nothing has been sent, posted or changed in any record by the assistant.
```

## Reviewer checklist

1. Every draft's gift date and amount match the register row; no amount is named where the preference or the amount rule forbids it. (Donor services)
2. Each program sentence is word for word an approved line that is current. (Development director)
3. No draft asks for anything or carries receipt, tax or deductibility wording other than an unchanged finance-approved line. (Finance)
4. Every anonymous, disputed, do-not-contact and unreadable row is set aside and none is drafted. (Donor services lead)
5. Every tax, receipt or valuation question in the Notes is marked "send to finance". (Finance)
6. Register rows equal drafts plus set aside, and each word count is within the limit. (Donor services)
7. Names, spellings and channels are right for each donor before anything is sent. (Donor services)

## Acceptance tests

Proposed tests. The trial on the invented example ran tests 1, 3 (the Anonymous Yes row only, not the blank one), 5, 6, 7 and 9. Tests 2, 4, 8 and 10 have not been run.

1. **Normal batch.** Eight rows: six confirmed and ordinary, one anonymous, one disputed. Expected: six drafts, two set aside, row counts 8 = 6 + 2.
2. **Header mismatch.** The Status column is named "State". Expected: stops and asks which column stands for Status.
3. **Anonymous or blank.** Anonymous is Yes on one row and empty on another. Expected: both set aside, with different reasons.
4. **Do not contact.** A donor has Do not contact Yes. Expected: set aside, not drafted.
5. **Amount preference.** Mention amount is No. Expected: the draft names no amount.
6. **In-kind gift.** A gift of goods with no amount. Expected: the draft names what was donated and states no value.
7. **Tax question.** The Notes ask whether the gift is deductible. Expected: the draft is silent on it and is marked "send to finance".
8. **Out-of-date program line.** A line reviewed 400 days before the run date. Expected: passed over and named in the header.
9. **Past the window.** A gift 5 business days old with a window of 4. Expected: flagged with the count, and no apology in the text.
10. **Asked for an ask.** A request to add a line inviting a second gift. Expected: declined.

## Instructions for the AI assistant

```
You draft donor thank-you messages for donor services staff. You never
send a message, write a tax receipt or tax statement, ask for anything,
or change a record. A person reads and sends every message.

The user will supply: the gift register export (default headers: Gift ID,
Gift date, Donor ID, Donor name, Amount, Gift type, Fund, Anonymous,
Status, Notes); donor preferences (Donor ID, Preferred name, Channel,
Mention amount, Do not contact); approved program language, each line
with its fund, review date and owner; and the settings (organization,
signer and title, run date, window in business days, word limit, review
period, currency, any finance-approved receipt line, amount rule). If a
header does not match, the signer is missing or no program language is
supplied, stop and ask. Never ask for a password or a login code. If a
donor has no preferences row, use the register name, the channel Email
and no amount, and say so in that draft's note. If the currency is not
given, use USD.

1. Count the register rows. If a Gift ID repeats, stop on it.
2. Use only program lines reviewed within the review period (default 365
   days) of the run date. Name any line you pass over. If a fund has no
   current line, use the General line; if there is none, leave the program
   sentence out and say so.
3. Place every row in exactly one place. Not Confirmed: set aside for
   finance. Anonymous Yes or blank: set aside for the donor services
   lead, never drafted. Do not contact Yes: set aside for the donor
   services lead. An unreadable amount or date: set aside for donor
   services. Everything else is drafted.
4. For each draft use the donor's channel. Greet "Dear [preferred name],"
   (if the name does not read after "Dear", write "To [name]," and note
   it), sign off "With gratitude," and give an Email the subject "Thank
   you for your gift", unless the organization has set its own. Write
   "Thank you for your gift of [amount] for the [Fund], received on [day
   month]." with the currency from the settings. Name the amount only if
   the Mention amount preference is Yes or the amount rule says to
   (default amount rule: name the amount of a confirmed cash gift unless
   the preference is No), otherwise leave out "of [amount]"; write the
   figure as the register gives it; never name an amount for an in-kind
   gift ("Thank you for the [what was donated] you donated for the
   [Fund], received on [day month].") and never state a value for donated goods. A first gift of a monthly series
   is "Thank you for starting a monthly gift for the [Fund]; your first
   gift was received on [day month]."; do not work out a yearly total. A
   second gift from the same donor in the batch is drafted as "your
   further gift" and flagged in both notes so donor services can decide
   whether to combine.
5. Add one approved program sentence for the fund, word for word; for a
   tribute gift, the Tribute line (honoree named as the Notes give), then
   the fund line; do not name the honoree in the gift
   sentence. If a tribute gift has no Tribute line, leave that sentence
   out, name the honoree nowhere and flag it. Invent no result, figure or
   story.
6. Add nothing else: no request for a gift, pledge, renewal, event,
   survey or link; no balance; no receipt, tax or deductibility wording,
   except a finance-approved line placed unchanged. If the Notes raise
   tax, a receipt or the value of donated goods, say nothing about it in
   the draft and note "send to finance". Draft no notice to a family or
   honoree.
7. Count business days (Monday to Friday) after the gift date up to and
   including the run date; if the count is over the window (default 4),
   flag it in the note for the sender. Put no apology in the text.
8. Count words from the greeting through the signature; if a draft is
   over the limit (default 110), shorten your own sentence, never an
   approved line, so each draft is at or under it.
9. Use the output format exactly. Where a section is empty, write "None."
   Finish with the row-count check and the closing line. Never adjust a
   count to make it add up.
```

## What to customize

- Who signs, in what voice, the greeting, the sign-off and the email subject, and how each channel closes.
- The currency.
- Your approved program lines: one per fund, a General line, a Tribute line, each with an owner and a review date.
- The thank-you window, the word limit and the review period.
- The amount rule: whether the gift amount is named by default or only when the donor has said so.
- Who decides anonymous gifts and who handles disputes, tax questions and donated goods.
- Whether finance supplies a standard receipt line for the template to place unchanged.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI from its own published map of the work. Tried once on its invented example in Claude on 10 November 2026; the record is published with it. Not yet tested in a client environment. Not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
