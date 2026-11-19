# Get Polymarket event odds

Automatically get Polymarket event odds on polymarket.com. Current odds of every outcome of a Polymarket event, by event URL or slug. For each outcome: its Yes and No price (0 to 1, the market's quoted price, not the last trade), best bid and ask, last trade price, volume and liquidity in USD, end date, and whether it is closed. Also returns the event's title, end date, total volume and liquidity. A single-question event returns one outcome. Throws if the slug matches no event.

- Site: polymarket.com
- Address: `reduck/polymarket.com/get_event_odds`
- Updated: 2026-11-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/polymarket.com/get_event_odds`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/polymarket.com/get_event_odds
```

## Input

- `url` (string, required): Event URL (https://polymarket.com/event/<slug>) or bare slug.

## Output

- `slug` (string, required)
- `event` (string, required)
- `outcomes` (array, required)
- `url` (string, optional)
- `end_date` (string | null, optional)
- `volume_usd` (number | null, optional)
- `liquidity_usd` (number | null, optional)

## FAQ

### What does "Get Polymarket event odds" do?

Current odds of every outcome of a Polymarket event, by event URL or slug. For each outcome: its Yes and No price (0 to 1, the market's quoted price, not the last trade), best bid and ask, last trade price, volume and liquidity in USD, end date, and whether it is closed. Also returns the event's title, end date, total volume and liquidity. A single-question event returns one outcome. Throws if the slug matches no event.

### How do I automatically get Polymarket event odds on polymarket.com?

Ask an AI agent connected to Reduck to run reduck/polymarket.com/get_event_odds, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/polymarket.com/get_event_odds

### Is there a polymarket.com API to get Polymarket event odds?

You do not need one. "Get Polymarket event odds" drives the real polymarket.com pages in a browser, so it works whether or not polymarket.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, slug, event, end_date, outcomes, volume_usd, liquidity_usd.

### Do I need to be logged in to polymarket.com?

No. It only uses pages of polymarket.com that are reachable without signing in.

### Does it change anything on polymarket.com, or only read data?

It only reads. It looks things up on polymarket.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/polymarket.com/get_event_odds, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/polymarket.com/get_event_odds

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/polymarket.com/get_event_odds
