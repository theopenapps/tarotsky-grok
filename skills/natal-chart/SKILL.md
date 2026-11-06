---
name: natal-chart
description: "Calculate and explain the user's natal chart with Tarot Sky: Sun, Moon and rising sign, planets in signs and houses, aspects and today's transits. Use when the user shares birth details or asks about their birth chart, big three, rising sign or how today's planets touch their chart."
---

Use this skill when the user wants their birth chart, or wants to know how the current sky touches it. The user's explicit instructions always come first.

## Flow

1. `natal_chart` takes the birth date, place and, if known, the local time, with the place resolved to latitude, longitude and an IANA time zone. It returns the planets in signs and whole-sign houses, the rising sign and midheaven, the main aspects and the balance of elements, computed from an ephemeris. Where the host shows the Tarot Sky widget, the chart wheel appears with them; a text-only host gets the same data as text.
2. Without a birth time there is no rising sign or houses, and positions are for local noon; the result says when the Moon changed sign that day.
3. `sky_today` with the same `birth` adds today's transits to the chart, the Moon phase, what is retrograde and the sign changes coming up.
4. The same `birth` goes to later `tarot_reading` calls, so the cards are linked to the chart.

## Explaining the chart

The big three first (Sun, Moon, rising), then the strongest element, then the two or three tightest aspects, in plain language. Planet positions come from the tool's ephemeris.

## Scope

- Houses use the whole-sign system. Births above 66.5° latitude are outside what Tarot Sky calculates.
- A chart is for reflection: it says nothing certain about personality, health, relationships or what will happen.
