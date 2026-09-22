# Get Polymarket market trades

Automatically get Polymarket market trades on polymarket.com. Latest trades for one (sub-)market of a Polymarket event, by event URL or slug. For multi-outcome events (e.g. "World Cup Winner"), `outcome` picks the sub-market ("Switzerland"); each trade's own outcome is then Yes/No on that binary market — so a bet backing the outcome is either a buy of Yes or a sell of No. Returns event, market, conditionId, n, and trades (time, side, outcome, price, shares, amountUsd, user, wallet, tx), newest first.

- Site: polymarket.com
- Address: `reduck/polymarket.com/get_market_trades`
- Updated: 2026-08-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/polymarket.com/get_market_trades`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/polymarket.com/get_market_trades
```

## Input

- `url` (string, required): Event URL (https://polymarket.com/event/<slug>) or bare slug.
- `limit` (number, optional): Max trades to return.
- `outcome` (string, optional): Sub-market to select in a multi-outcome event, matched case-insensitively against each market's title (e.g. "Switzerland"). Omit for single-market events.

## Output

- `n` (number, required)
- `event` (string, required)
- `market` (string, required)
- `trades` (array, required)
- `conditionId` (string, required)

## FAQ

### What does "Get Polymarket market trades" do?

Latest trades for one (sub-)market of a Polymarket event, by event URL or slug. For multi-outcome events (e.g. "World Cup Winner"), `outcome` picks the sub-market ("Switzerland"); each trade's own outcome is then Yes/No on that binary market — so a bet backing the outcome is either a buy of Yes or a sell of No. Returns event, market, conditionId, n, and trades (time, side, outcome, price, shares, amountUsd, user, wallet, tx), newest first.

### How do I automatically get Polymarket market trades on polymarket.com?

Ask an AI agent connected to Reduck to run reduck/polymarket.com/get_market_trades, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/polymarket.com/get_market_trades

### Is there a polymarket.com API to get Polymarket market trades?

You do not need one. "Get Polymarket market trades" drives the real polymarket.com pages in a browser, so it works whether or not polymarket.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: limit, outcome.

### What does it return?

It returns n, event, market, trades, conditionId.

### Do I need to be logged in to polymarket.com?

No. It only uses pages of polymarket.com that are reachable without signing in.

### Does it change anything on polymarket.com, or only read data?

Unknown: its author has not declared whether it changes anything on polymarket.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/polymarket.com/get_market_trades, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/polymarket.com/get_market_trades

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/polymarket.com/get_market_trades
