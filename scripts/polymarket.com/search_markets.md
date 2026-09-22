# Search Polymarket markets

Automatically search Polymarket markets on polymarket.com. Search Polymarket events by keyword. Returns matching markets with title, URL, volume, end date, and current top outcome.

- Site: polymarket.com
- Address: `reduck/polymarket.com/search_markets`
- Updated: 2026-07-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/polymarket.com/search_markets`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/polymarket.com/search_markets
```

## Input

- `query` (string, required): Keyword to search Polymarket events, e.g. "Fed rates"
- `limit` (integer, optional): Max markets to return. Default 20.

## Output

- `query` (string, optional)
- `markets` (array, optional)
- `results_total` (integer | null, optional)

## FAQ

### What does "Search Polymarket markets" do?

Search Polymarket events by keyword. Returns matching markets with title, URL, volume, end date, and current top outcome.

### How do I automatically search Polymarket markets on polymarket.com?

Ask an AI agent connected to Reduck to run reduck/polymarket.com/search_markets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/polymarket.com/search_markets

### Is there a polymarket.com API to search Polymarket markets?

You do not need one. "Search Polymarket markets" drives the real polymarket.com pages in a browser, so it works whether or not polymarket.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: limit.

### What does it return?

It returns query, markets, results_total.

### Do I need to be logged in to polymarket.com?

No. It only uses pages of polymarket.com that are reachable without signing in.

### Does it change anything on polymarket.com, or only read data?

Unknown: its author has not declared whether it changes anything on polymarket.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/polymarket.com/search_markets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/polymarket.com/search_markets

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/polymarket.com/search_markets
