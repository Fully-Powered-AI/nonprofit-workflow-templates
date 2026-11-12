# Donor thank-you drafts: one trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs are the invented example in [example.md](example.md) (Harbor Lane Food Pantry, eight gifts, six donor preferences, four approved program lines, the settings). No client data was used. The run followed the instruction block and the output format in the member template as they now stand.

This is the third run, made the same day. The first run was on an earlier wording of the block that left the greeting, sign-off, subject, currency and the tribute and monthly-gift sentences open. The second run, on a revised block, matched the published example exactly. Review then asked for small clarifications to the block (the default amount rule, the default window and word limit, how business days are counted, the tribute-line order, a draft exactly at the word limit) and for the check line to follow the output format; this run was made on the clarified block, and this record replaces the second. It was not blind: the published example and the earlier runs' observations were in view when the block was revised and when this run was made, so the close match with the published example below is expected and is not independent evidence that the block is clear.

## What came out

Six drafts and two set-aside rows. The full batch page:

```
DONOR THANK-YOU DRAFTS: Harbor Lane Food Pantry
Status: Drafts for Marcus Ibarra, Donor Services. Nothing has been sent.
Run date: Monday 9 November 2026. Register rows: 8. Drafts: 6. Set aside: 2.
Program language: P1, P2 and P3 used; G1 current, not needed (every fund has a line). All inside the 365-day review period.
Finance receipt line: none supplied, so no receipt wording appears anywhere.

DRAFTS

1. G-2041, Tessa Brandt (D-118). Email. Program line: P1.
Subject: Thank you for your gift

Dear Tessa,

Thank you for your gift of $250.00 for the Food Pantry, received on 2 November. Your gift helps us put fresh and shelf-stable food in the hands of neighbors every week we are open.

With gratitude,
Marcus Ibarra
Donor Services, Harbor Lane Food Pantry

Note for the sender: past the 4-business-day window (5 business days since 2 November). This donor has a further gift in this batch (item 5).

2. G-2042, Company K (D-131). Letter. Program line: P2.

Dear Company K team,

Thank you for your gift of $1500.00 for the Winter Coat Drive, received on 2 November. Coats given through this drive go to neighbors before the cold sets in, at our Thursday distribution.

With gratitude,
Marcus Ibarra
Donor Services, Harbor Lane Food Pantry

Note for the sender: past the window (5 business days).

3. G-2043, Hollis Meyer (D-140). Email. Program line: P1.
Subject: Thank you for your gift

Dear Hollis,

Thank you for starting a monthly gift for the Food Pantry; your first gift was received on 3 November. Your gift helps us put fresh and shelf-stable food in the hands of neighbors every week we are open.

With gratitude,
Marcus Ibarra
Donor Services, Harbor Lane Food Pantry

Note for the sender: the amount is not named because the donor's preference for mentioning it is No.

4. G-2046, Wendell Park (D-171). Card. Program lines: P3, P1.

Dear Wendell,

Thank you for your gift of $100.00 for the Food Pantry, received on 4 November. Your gift in memory of Ruth Park is a lasting way to remember them. Your gift helps us put fresh and shelf-stable food in the hands of neighbors every week we are open.

With gratitude,
Marcus Ibarra
Donor Services, Harbor Lane Food Pantry

Note for the sender: the donor asks whether the gift is tax deductible. The draft is silent on it. Send to finance. No notice to Ruth Park's family is drafted.

5. G-2047, Tessa Brandt (D-118). Email. Program line: P1.
Subject: Thank you for your gift

Dear Tessa,

Thank you for your further gift of $60.00 for the Food Pantry, received on 5 November. Your gift helps us put fresh and shelf-stable food in the hands of neighbors every week we are open.

With gratitude,
Marcus Ibarra
Donor Services, Harbor Lane Food Pantry

Note for the sender: second gift in this batch from D-118; G-2041 is item 1. Decide whether to send both or combine them.

6. G-2048, Gordon Ng (D-190). Email. Program line: P2.
Subject: Thank you for your gift

Dear Gordon,

Thank you for the 12 winter coats you donated for the Winter Coat Drive, received on 5 November. Coats given through this drive go to neighbors before the cold sets in, at our Thursday distribution.

With gratitude,
Marcus Ibarra
Donor Services, Harbor Lane Food Pantry

Note for the sender: no value is stated for donated goods, and none is named in the draft. Any question about value goes to finance.

SET ASIDE

- G-2044, anonymous gift (D-152), 3 November. Anonymous is Yes. No draft. Donor services lead decides whether any acknowledgement goes out and in what form.
- G-2045, Ines Calder (D-160), 4 November. Status is Disputed (the donor says the card was charged twice). No draft until the amount is confirmed. Finance decides.

CHECK

Register rows 8 = drafts 6 + set aside 2. Gift IDs drafted: G-2041, G-2042, G-2043, G-2046, G-2047, G-2048; set aside: G-2044, G-2045. Word counts, greeting through signature: item 1, 46; item 2, 47; item 3, 50; item 4, 60; item 5, 47; item 6, 47; limit 110.
Asks: none of the drafts asks for a gift, a pledge, an event or a click. Tax and receipt wording: none in any draft.

Prepared for Marcus Ibarra. Nothing has been sent, posted or changed in any record by the assistant.
```

## What was observed

- **Every required part was produced:** the header, six drafts with notes, the set-aside list, the check and the closing line. Counts added up (8 = 6 + 2). No stop condition was met.
- **Differences from the published example:** none in wording. The word counts match (46, 47, 50, 60, 47, 47, all within 110). The check line now lists Gift IDs as "drafted" and "set aside" with the register's G- prefix, as the output format says, and the amount for item 2 is written as the register gives it ($1500.00), which the clarified block states.
- **Points the first run found, and what this run showed:**
  - Greeting, sign-off and subject: the revised block names defaults, and this run used them. A different run could still choose its own wording if the person overrides them.
  - Currency: the settings now say USD and the block says to take it from the settings, so the "$" sign is no longer a guess.
  - Tribute gift: the honoree appeared once, in the approved tribute line.
  - Monthly gift: the sentence follows the block's wording ("your first gift was received on 3 November").
  - Company K: the preferred name was changed in the input to "Company K team", so "Dear Company K team," reads normally. The fall-back greeting "To [name]," for a name that does not read after "Dear" was not exercised.
  - The header lists G1 as current and not needed, and the card draft says only "Card", as the input does.
- **Where the instructions are still open to a guess:**
  - Business days are now stated in the block as after the gift date up to and including the run date; this run followed that, and a gift on Monday 2 November with a run on Monday 9 November gives 5. That point is no longer open.
  - Whether a Subject line counts towards the word limit. This run counted from the greeting, as the template says.
  - The order of the two approved lines in a tribute draft was taken from the block (Tribute line, then fund line).
  - The run date may fall on a day the gift was already thanked in a previous batch; the template has no way to know.
- **Not exercised by this run:** a header mismatch, a stale program line, a do-not-contact donor, a missing preferences row, a fund with no line, a tribute gift with no Tribute line, a request for an ask. Acceptance tests 2, 4, 8 and 10 have not been run; test 3 was run on the Anonymous Yes row only.
- **What this does not show:** it is one run, by one model, on invented data, made with the example in view. It is not a test in a real environment and says nothing about how the workflow template performs for a real organization.
