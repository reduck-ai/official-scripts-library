# Get TradingView ticker overview

Automatically get TradingView ticker overview on tradingview.com. Read a TradingView symbol page: company name and description, displayed price with currency and change, session status, the security's isin/cusip/figi identifiers, asset category and the market sector breadcrumb path. Anonymous, read-only. Accepts a bare ticker (TradingView redirects it to the primary listing) or an exchange-qualified one such as "NASDAQ:AAPL".

- Site: tradingview.com
- Address: `reduck/tradingview.com/get_ticker_overview`
- Updated: 2026-09-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tradingview.com/get_ticker_overview`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tradingview.com/get_ticker_overview
```

## Input

- `symbol` (string, required): Ticker, either bare ("AAPL") or exchange-qualified ("NASDAQ:AAPL", "LSE:BARC"). A bare ticker is resolved by TradingView's own redirect to whichever listing it treats as primary — the listing actually returned is reported as resolvedSymbol. Either ":" or "-" is accepted as the exchange separator.

## Output

- `url` (string, required)
- `name` (string | null, required): Instrument / company name, e.g. "Apple Inc.".
- `price` (number | null, required): Last displayed price for this symbol, scoped to the page's own header ticker. The page reuses the same markup for a related-symbols rail, so this is deliberately scoped rather than taken from the first match.
- `symbol` (string, required): The symbol as requested, echoed for joining.
- `currency` (string | null, required)
- `resolvedSymbol` (string, required): The exchange-qualified symbol TradingView actually served, read from the page itself. Differs from `symbol` whenever a bare ticker was passed, and also for instruments whose url drops the exchange segment, so join on this.
- `category` (string | null, optional): Asset category from structured data, e.g. "Stock", "Cryptocurrency".
- `changeText` (string | null, optional): Absolute price change exactly as rendered (e.g. "+3.25"), original minus sign preserved. Null is legitimate: some instrument pages render only the percentage.
- `sectorPath` (array, optional): The page's breadcrumb trail, which is TradingView's market taxonomy for the symbol, e.g. ["Markets","USA","Stocks","Electronic Technology","Telecommunications Equipment","AAPL"].
- `symbolType` (string | null, optional): TradingView's asset type for the symbol, e.g. "stock", "spot", "forex".
- `description` (string | null, optional): Business description from the page's structured data. Null for instrument types that carry none.
- `identifiers` (object, optional): Security identifiers from structured data, keyed by type (isin, cusip, figi, tickerSymbol as the page labels them). Crypto and forex publish a different set (base/quote asset) or none, so this map is intentionally open-ended.
- `snapshotAsOf` (string | null, optional): The structured data's priceValidUntil timestamp — the session the snapshotPrice belongs to.
- `changePercent` (number | null, optional): Change in percent as a number. The page renders the minus sign as U+2212, which is normalised to a plain hyphen before parsing.
- `sessionStatus` (string | null, optional): Market session label as rendered and localised ("Pre-market", "Market open"). Verbatim, not normalised.
- `snapshotPrice` (string | null, optional): Price from the page's structured data, as a decimal string. This is a session snapshot, not the live tick — it can differ from `price` when the displayed quote is pre- or post-market. Paired with snapshotAsOf.
- `changePercentText` (string | null, optional): Percentage change exactly as rendered (e.g. "+1.00%").

## FAQ

### What does "Get TradingView ticker overview" do?

Read a TradingView symbol page: company name and description, displayed price with currency and change, session status, the security's isin/cusip/figi identifiers, asset category and the market sector breadcrumb path. Anonymous, read-only. Accepts a bare ticker (TradingView redirects it to the primary listing) or an exchange-qualified one such as "NASDAQ:AAPL".

### How do I automatically get TradingView ticker overview on tradingview.com?

Ask an AI agent connected to Reduck to run reduck/tradingview.com/get_ticker_overview, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tradingview.com/get_ticker_overview

### Is there a tradingview.com API to get TradingView ticker overview?

You do not need one. "Get TradingView ticker overview" drives the real tradingview.com pages in a browser, so it works whether or not tradingview.com offers an API for this.

### What information do I need to provide?

Required: symbol.

### What does it return?

It returns url, name, price, symbol, category, currency, changeText, sectorPath, symbolType, description, identifiers, snapshotAsOf, changePercent, sessionStatus, snapshotPrice, resolvedSymbol, changePercentText.

### Do I need to be logged in to tradingview.com?

No. It only uses pages of tradingview.com that are reachable without signing in.

### Does it change anything on tradingview.com, or only read data?

It only reads. It looks things up on tradingview.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tradingview.com/get_ticker_overview, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tradingview.com/get_ticker_overview

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tradingview.com/get_ticker_overview
