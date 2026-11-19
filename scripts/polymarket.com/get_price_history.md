# Get Polymarket price history

Automatically get Polymarket price history on polymarket.com. Price series of one outcome of a Polymarket event, as the event page's chart shows it, over 1 day, 1 week, 1 month or the whole market life. Takes the event URL or slug, the outcome name for multi-outcome events, and Yes or No. Returns the outcome, side, interval and points (time, price from 0 to 1), oldest first, plus the first and last price. Throws if the event or outcome is not found.

- Site: polymarket.com
- Address: `reduck/polymarket.com/get_price_history`
- Updated: 2026-11-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/polymarket.com/get_price_history`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/polymarket.com/get_price_history
```

## Input

- `url` (string, required): Event URL (https://polymarket.com/event/<slug>) or bare slug.
- `side` (string, optional)
- `outcome` (string, optional): Outcome to read in a multi-outcome event, matched case-insensitively against its name (e.g. "Le Pen"). Omit for single-question events.
- `interval` (string, optional)

## Output

- `side` (string, required)
- `event` (string, required)
- `points` (array, required)
- `outcome` (string, required)
- `interval` (string, required)
- `last_price` (number | null, optional)
- `first_price` (number | null, optional)

## FAQ

### What does "Get Polymarket price history" do?

Price series of one outcome of a Polymarket event, as the event page's chart shows it, over 1 day, 1 week, 1 month or the whole market life. Takes the event URL or slug, the outcome name for multi-outcome events, and Yes or No. Returns the outcome, side, interval and points (time, price from 0 to 1), oldest first, plus the first and last price. Throws if the event or outcome is not found.

### How do I automatically get Polymarket price history on polymarket.com?

Ask an AI agent connected to Reduck to run reduck/polymarket.com/get_price_history, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/polymarket.com/get_price_history

### Is there a polymarket.com API to get Polymarket price history?

You do not need one. "Get Polymarket price history" drives the real polymarket.com pages in a browser, so it works whether or not polymarket.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: side, outcome, interval.

### What does it return?

It returns side, event, points, outcome, interval, last_price, first_price.

### Do I need to be logged in to polymarket.com?

No. It only uses pages of polymarket.com that are reachable without signing in.

### Does it change anything on polymarket.com, or only read data?

It only reads. It looks things up on polymarket.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/polymarket.com/get_price_history, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/polymarket.com/get_price_history

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/polymarket.com/get_price_history
