# Search Wise transactions

Automatically search Wise transactions on wise.com. Search a Wise profile's transactions by merchant/name (server-side), optionally narrowed to a date range. Returns id, title, amount, date, status and whether a receipt is attached.

- Site: wise.com
- Address: `reduck/wise.com/search_transactions`
- Updated: 2026-08-07 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/wise.com/search_transactions`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/wise.com/search_transactions
```

## Input

- `search` (string, required): Text to search (merchant/description), e.g. "OpenAI". Leave empty to list recent transactions unfiltered.
- `to` (string, optional): Optional inclusive end date ISO (YYYY-MM-DD).
- `from` (string, optional): Optional inclusive start date ISO (YYYY-MM-DD). Filters on the transaction's finished date.

## Output

- `count` (integer, required)
- `transactions` (array, required)

## FAQ

### What does "Search Wise transactions" do?

Search a Wise profile's transactions by merchant/name (server-side), optionally narrowed to a date range. Returns id, title, amount, date, status and whether a receipt is attached.

### How do I automatically search Wise transactions on wise.com?

Ask an AI agent connected to Reduck to run reduck/wise.com/search_transactions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wise.com/search_transactions

### Is there a wise.com API to search Wise transactions?

You do not need one. "Search Wise transactions" drives the real wise.com pages in a browser, so it works whether or not wise.com offers an API for this.

### What information do I need to provide?

Required: search. Optional: to, from.

### What does it return?

It returns count, transactions.

### Do I need to be logged in to wise.com?

Yes. It acts as you on wise.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the wise.com cookies saved by the Reduck extension.

### Does it change anything on wise.com, or only read data?

It only reads. It looks things up on wise.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/wise.com/search_transactions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wise.com/search_transactions

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/wise.com/search_transactions
