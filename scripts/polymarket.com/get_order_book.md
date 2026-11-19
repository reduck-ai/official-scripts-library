# Get Polymarket order book

Automatically get Polymarket order book on polymarket.com. Order book of one outcome of a Polymarket event: best bid and ask, spread, midpoint, and the resting bids and asks (price from 0 to 1, size in shares) nearest the spread, with total shares and USD on each side. Takes the event URL or slug, the outcome name for multi-outcome events, Yes or No, and how many price levels to return. A market with no orders returns empty sides and null best prices. Throws if the event or outcome is not found.

- Site: polymarket.com
- Address: `reduck/polymarket.com/get_order_book`
- Updated: 2026-11-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/polymarket.com/get_order_book`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/polymarket.com/get_order_book
```

## Input

- `url` (string, required): Event URL (https://polymarket.com/event/<slug>) or bare slug.
- `side` (string, optional)
- `levels` (integer, optional): Price levels to return on each side, nearest the spread first.
- `outcome` (string, optional): Outcome in a multi-outcome event, matched case-insensitively against its name. Omit for single-question events.

## Output

- `asks` (array, required)
- `bids` (array, required)
- `side` (string, required)
- `event` (string, required)
- `outcome` (string, required)
- `spread` (number | null, optional)
- `best_ask` (number | null, optional)
- `best_bid` (number | null, optional)
- `midpoint` (number | null, optional)
- `tick_size` (number | null, optional)
- `timestamp` (string | null, optional)
- `ask_depth_usd` (number, optional)
- `bid_depth_usd` (number, optional)
- `ask_depth_shares` (number, optional)
- `ask_levels_total` (integer, optional)
- `bid_depth_shares` (number, optional)
- `bid_levels_total` (integer, optional)

## FAQ

### What does "Get Polymarket order book" do?

Order book of one outcome of a Polymarket event: best bid and ask, spread, midpoint, and the resting bids and asks (price from 0 to 1, size in shares) nearest the spread, with total shares and USD on each side. Takes the event URL or slug, the outcome name for multi-outcome events, Yes or No, and how many price levels to return. A market with no orders returns empty sides and null best prices. Throws if the event or outcome is not found.

### How do I automatically get Polymarket order book on polymarket.com?

Ask an AI agent connected to Reduck to run reduck/polymarket.com/get_order_book, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/polymarket.com/get_order_book

### Is there a polymarket.com API to get Polymarket order book?

You do not need one. "Get Polymarket order book" drives the real polymarket.com pages in a browser, so it works whether or not polymarket.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: side, levels, outcome.

### What does it return?

It returns asks, bids, side, event, spread, outcome, best_ask, best_bid, midpoint, tick_size, timestamp, ask_depth_usd, bid_depth_usd, ask_depth_shares, ask_levels_total, bid_depth_shares, bid_levels_total.

### Do I need to be logged in to polymarket.com?

No. It only uses pages of polymarket.com that are reachable without signing in.

### Does it change anything on polymarket.com, or only read data?

It only reads. It looks things up on polymarket.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/polymarket.com/get_order_book, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/polymarket.com/get_order_book

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/polymarket.com/get_order_book
