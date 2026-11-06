---
name: week-ahead
description: "Start the week with Tarot Sky: the week's Moon, retrogrades and sign changes, then a three-card week-ahead spread tied to them. Use when the user wants to start their week, asks for a weekly reading, or asks what the sky holds for the coming days."
---

Use this skill when the user starts their week with Tarot Sky ("start my week", "weekly reading"). The user's explicit instructions always come first.

## Flow

1. `sky_today`, with the user's `birth` when it is known, gives the Moon's phase and sign, what is retrograde, the sign changes and stations coming up, and the transits to the user's chart.
2. `tarot_reading` with the spread `week-ahead` lays out three cards: what to lean into, what to watch and what to let go. Cards from the user's own deck and a virtual draw both work.
3. The reading ties each card to one event in the week ahead, in about 250 words, and ends with one reflective question.

## Scope

- For reflection: the week ahead is described as what to notice, not as what will happen.
- `tarot_spreads` lists the other spreads, for a different question.
