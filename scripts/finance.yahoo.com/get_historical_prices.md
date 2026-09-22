# Get Historical Prices

Automatically get Historical Prices on finance.yahoo.com. OHLCV price history for a single Yahoo Finance symbol (stock, crypto, index, future) over a range/interval, matching the site's own chart affordance.

- Site: finance.yahoo.com
- Address: `reduck/finance.yahoo.com/get_historical_prices`
- Updated: 2026-09-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/finance.yahoo.com/get_historical_prices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/finance.yahoo.com/get_historical_prices
```

## Input

- `range` (string, required): Matches the site's own chart range buttons (1D/5D/1M/6M/YTD/1Y/5Y/All, plus a few extra Yahoo also accepts).
- `symbol` (string, required): Single Yahoo Finance ticker symbol, e.g. AAPL, BTC-USD, CL=F, ^VIX. The chart endpoint is single-symbol only.
- `interval` (string, required): Candle granularity. Fine intervals (e.g. 1m) are only available for short ranges — Yahoo enforces this server-side and the script surfaces its error verbatim on a mismatch.

## Output

- `range` (string, required)
- `symbol` (string, required)
- `candles` (array, required)
- `interval` (string, required)
- `currency` (string | null, optional)
- `timezone` (string | null, optional)
- `gmtoffset` (number | null, optional)
- `exchangeName` (string | null, optional)
- `instrumentType` (string | null, optional)

## FAQ

### What does "Get Historical Prices" do?

OHLCV price history for a single Yahoo Finance symbol (stock, crypto, index, future) over a range/interval, matching the site's own chart affordance.

### How do I automatically get Historical Prices on finance.yahoo.com?

Ask an AI agent connected to Reduck to run reduck/finance.yahoo.com/get_historical_prices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/finance.yahoo.com/get_historical_prices

### Is there a finance.yahoo.com API to get Historical Prices?

You do not need one. "Get Historical Prices" drives the real finance.yahoo.com pages in a browser, so it works whether or not finance.yahoo.com offers an API for this.

### What information do I need to provide?

Required: symbol, range, interval.

### What does it return?

It returns range, symbol, candles, currency, interval, timezone, gmtoffset, exchangeName, instrumentType.

### Do I need to be logged in to finance.yahoo.com?

No. It only uses pages of finance.yahoo.com that are reachable without signing in.

### Does it change anything on finance.yahoo.com, or only read data?

It only reads. It looks things up on finance.yahoo.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/finance.yahoo.com/get_historical_prices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/finance.yahoo.com/get_historical_prices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/finance.yahoo.com/get_historical_prices
