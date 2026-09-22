# Sales Navigator: search accounts

Automatically search accounts on linkedin.com. Search LinkedIn Sales Navigator company accounts by keywords, headquarters geography, and headcount, paginated 25 per page via a 0-based start offset. Returns total, count, start, and accounts (accountId, companyName, industry, employee count and range, description, list/saved status, spotlight badges, salesAccountUrl). Requires a Sales Navigator seat.

- Site: linkedin.com
- Address: `reduck/linkedin.com/sales_navigator_search_accounts`
- Updated: 2026-09-03 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/sales_navigator_search_accounts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_search_accounts
```

## Input

- `start` (integer, optional): 0-based result offset; the page returns 25. Pass 0, 25, 50, ... to paginate.
- `keywords` (string, optional): Free-text keyword box (company name / terms).
- `geography` (string, optional): HQ location, free text resolved to a region id (e.g. "France", "Paris", "United States").
- `companyHeadcount` (array, optional): Company headcount buckets (OR).

## Output

- `count` (integer, required)
- `start` (integer, required)
- `total` (integer, required)
- `accounts` (array, required)
- `totalDisplay` (string | null, optional)

## FAQ

### What does "Sales Navigator: search accounts" do?

Search LinkedIn Sales Navigator company accounts by keywords, headquarters geography, and headcount, paginated 25 per page via a 0-based start offset. Returns total, count, start, and accounts (accountId, companyName, industry, employee count and range, description, list/saved status, spotlight badges, salesAccountUrl). Requires a Sales Navigator seat.

### How do I automatically search accounts on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_search_accounts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_search_accounts

### Is there a linkedin.com API to search accounts?

You do not need one. "Sales Navigator: search accounts" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: start, keywords, geography, companyHeadcount.

### What does it return?

It returns count, start, total, accounts, totalDisplay.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_search_accounts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_search_accounts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/sales_navigator_search_accounts
