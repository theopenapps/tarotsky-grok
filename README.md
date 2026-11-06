# Tarot and Birth Chart Readings by Tarot Sky

Tarot readings tied to your natal chart and today's planets, inside your AI assistant. Made by [The Open Apps, Inc.](https://apps.ambientapp.ai/)

Shuffle your own deck and tell the assistant what came up, or ask it to draw for you. Tarot Sky lays the cards out in their spread and gives each card's meaning upright or reversed, its symbols and its astrological correspondence. Share your birth date, place and (if you know it) time once, and it calculates your natal chart from an ephemeris and links every card to your chart and to where the planets are today. Your assistant writes the reading from that. In Grok and Cursor the answers come as text.

No account, no API key. Tarot Sky keeps nothing you send.

## Install

This repo is the plugin: it connects one remote MCP server and adds three skills.

| File | What it holds |
| --- | --- |
| `.cursor-plugin/plugin.json`, `.grok-plugin/plugin.json` | The plugin manifest (identical) |
| `mcp.json`, `.mcp.json` | The server: `https://tarotsky.ambientapp.ai/mcp/grok` |
| `skills/` | `card-reading`, `natal-chart`, `week-ahead` |

Any other MCP client can add `https://tarotsky.ambientapp.ai/mcp/grok` as a remote (Streamable HTTP) server with no credentials.

## Tools

| Tool | What it does | What it changes |
| --- | --- | --- |
| `tarot_start` | Lists the ways to start: cards drawn for a question, your own deck, your birth chart, today's sky | Nothing |
| `tarot_reading` | Reads a spread from the cards you drew, or draws them, with each card's meaning, symbols, correspondence and links to your chart and today's sky | Nothing |
| `tarot_card` | One card's upright and reversed meaning, symbols, a question to reflect on and its astrology | Nothing |
| `tarot_spreads` | The eight spreads and what each position means | Nothing |
| `natal_chart` | Sun, Moon and rising sign, planets in signs and whole-sign houses, aspects and the balance of elements | Nothing |
| `sky_today` | Today's planets, Moon phase, retrogrades, coming sign changes and transits to your chart | Nothing |
| `deck_design` | Picks the historical deck for your readings, with a tint, frame and colours, and returns a code to keep it (the art itself shows only in apps that display the Tarot Sky widget) | Nothing |

All seven tools only read: each one calculates an answer from what it is sent and keeps nothing between calls.

## Try

- "Use Tarot Sky to read the cards I drew: the Chariot, the Eight of Pentacles and the Knight of Wands reversed. What do they say about my work this month?"
- "Use Tarot Sky to show my birth chart. I was born 3 October 1991 at 16:00 in Lisbon."
- "Use Tarot Sky to tell me what's retrograde right now and what the Moon is doing."
- "Use Tarot Sky to lay out a Celtic Cross about moving cities."

## Limits

- For reflection and entertainment. Tarot Sky never predicts health, money, legal or other outcomes; yes/no questions are read as what to notice, not as a verdict.
- Houses use the whole-sign system. Without a birth time there is no rising sign or houses. Births above 66.5° latitude are not supported.
- Cards and charts are labelled in English; your assistant writes the reading in your language.
- The card art is public-domain: Pamela Colman Smith's 1909 drawings, Jean Dodal's Tarot de Marseille (about 1701) and Oswald Wirth's 1889 major arcana. Not affiliated with U.S. Games Systems.

## Links

- Docs: https://tarotsky.ambientapp.ai/docs
- Privacy: https://tarotsky.ambientapp.ai/privacy
- Terms: https://tarotsky.ambientapp.ai/terms
- Support: https://tarotsky.ambientapp.ai/support (support@theopenapps.com)

## License

MIT © The Open Apps, Inc. The license covers this repo's files. The Tarot Sky service is governed by its [terms](https://tarotsky.ambientapp.ai/terms).
