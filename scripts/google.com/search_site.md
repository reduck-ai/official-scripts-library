# Search Google

Automatically search Google on google.com. Run a Google search and return the page's organic result cards (title, url, site, byline, meta, snippet), with redirect wrappers already cleaned from urls. Runs logged out by default; if the browser happens to carry Google cookies, results are personalized to that account/IP.

- Site: google.com
- Address: `reduck/google.com/search_site`
- Updated: 2026-09-17 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/search_site`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/search_site
```

## Input

- `query` (string, required): Full Google query, e.g. 'site:linkedin.com/in Ex-UiPath' or any free-text search.
- `page` (integer, optional): Result page, 0 = first (maps to Google's &start=page*10), mirroring the SERP pager. Pages are deterministic under replay and disjoint across page numbers, so callers may fetch different pages concurrently and union the results. Note that results are personalised and geo-located to the browser's Google session, so ordering is stable only for a given account, IP and moment.
- `freshness` (string, optional): Canonical Google time filter (mapped to tbs=qdr:<value>). One of h (past hour), d (past 24h), w (past week), y (past year), m (past month), optionally with a multiplier: d2 = past 2 days, w3 = past 3 weeks, m6 = past 6 months, h5 = past 5 hours. Omit for all-time.
- `sortByDate` (boolean, optional): When true, sort results by date (newest first) instead of relevance (tbs=sbd:1). Combines with freshness.

## FAQ

### What does "Search Google" do?

Run a Google search and return the page's organic result cards (title, url, site, byline, meta, snippet), with redirect wrappers already cleaned from urls. Runs logged out by default; if the browser happens to carry Google cookies, results are personalized to that account/IP.

### How do I automatically search Google on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/search_site, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/search_site

### Is there a google.com API to search Google?

You do not need one. "Search Google" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, freshness, sortByDate.

### Do I need to be logged in to google.com?

No. It only uses pages of google.com that are reachable without signing in.

### Does it change anything on google.com, or only read data?

It only reads. It looks things up on google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/search_site, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/search_site

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/search_site
