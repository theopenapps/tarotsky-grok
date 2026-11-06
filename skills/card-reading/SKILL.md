---
name: card-reading
description: "Read tarot cards with Tarot Sky: a spread from cards the user drew from their own deck, or a virtual draw, tied to their birth chart and today's sky. Use when the user wants a tarot reading, names cards they drew, asks what a card means, or opens Tarot Sky without a clear request."
---

Use this skill for tarot readings with Tarot Sky. Tarot Sky computes and the assistant interprets: the tools return each card's meaning, symbols, astrological correspondence and plain-language links to the user's chart and today's sky, and the reading is written from those facts. The user's explicit instructions always come first.

## Flow

1. `tarot_start` shows the starts when the user opens Tarot Sky or asks what it can do without a clear request; the user's pick comes back as their next message.
2. For cards from the user's own deck, the spread comes first (`tarot_spreads` lists every spread's positions), then every card in position order, with the reversed ones marked. `tarot_reading` takes the spread and the cards.
3. For a virtual draw, `tarot_reading` takes the spread and no `cards`.
4. Birth details tie the reading to the user's chart: date, place and, if known, time, asked for once. The place is resolved to coordinates and an IANA time zone, so the user isn't asked for coordinates. The same `birth` goes to every later call in the conversation.
5. `tarot_card` explains one card outside a reading.

Spreads by question: `one-card` for a quick check-in, `three-card` for most questions, `week-ahead` to start a week, `crossroads` for a decision, `two-hearts` for a relationship, `mind-heart-action` or `celtic-cross` for something big, and `twelve-houses` for a full sweep that pairs with the chart.

## The reading

Each result's `guidance` gives a word count that scales with the spread and a suggested shape: a short sky report, each card in its position (meaning first, then the astrology links that add something), the patterns across the cards, and one reflective question to end. Where the Tarot Sky widget shows the cards, the reading interprets them rather than listing them.

## Scope

- Tarot and astrology here are for reflection and entertainment. A yes/no question is read as what to notice, not as a verdict. Readings make no predictions about illness, death, pregnancy, legal or money outcomes and give no health, legal or financial advice. If the user seems in distress, the person comes before the reading.
- `deck_design` changes the historical card art used in readings. Drawing new card pictures or making a personal deck is outside Tarot Sky.
