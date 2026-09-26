# Google Trends API: compare keywords and get related queries

Automatically compare keywords and get related queries on trends.google.com. An unofficial Google Trends API: compare up to 5 keywords' search interest over time and by region, and get their top and rising related queries, as data in one call. Google Trends explore for 1-5 keywords in one compare query: interest over time (shared scale), interest by region, per-region share %, related topics and queries (top + rising), for a given geo/date range/category/property.

- Site: trends.google.com
- Address: `reduck/trends.google.com/explore_keyword`
- Updated: 2026-09-25 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/trends.google.com/explore_keyword`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/trends.google.com/explore_keyword
```

## Input

- `keywords` (array, required): 1-5 search terms and/or Trends topic mids (e.g. "/g/11khcfz0y2") compared in a single query — values are relative to the shared peak, so this is the only way to compare terms. Terms must not contain commas (the site's own separator).
- `geo` (string, optional): ISO region code: "US", "FR", "US-CA"… Empty string = worldwide.
- `date` (string, optional): Trends range: "now 1-H", "now 4-H", "now 1-d", "now 7-d", "today 1-m", "today 3-m", "today 12-m", "today 5-y", "all", or explicit "YYYY-MM-DD YYYY-MM-DD".
- `category` (integer, optional): Trends category id (0 = all categories). Same ids as the site's category picker.
- `property` (string, optional): Search property: "" = web search, images, news, froogle (shopping), youtube.

## Output

- `geo` (string, required)
- `date` (string, required)
- `keywords` (array, required)
- `byKeyword` (array, required): Per-keyword panels, aligned with keywords. relatedTopics is null in compare mode — the site drops that panel when comparing.
- `regionShare` (array, required): Compare mode only (2+ keywords), else []: each keyword's share (%) of combined interest per region, shares[i] aligns with keywords[i].
- `interestOverTime` (array, required): Relative interest 0-100, shared scale across all keywords (100 = the overall peak). values[i] aligns with keywords[i]. Empty for insufficient volume.

## FAQ

### What does "Google Trends API: compare keywords and get related queries" do?

An unofficial Google Trends API: compare up to 5 keywords' search interest over time and by region, and get their top and rising related queries, as data in one call. Google Trends explore for 1-5 keywords in one compare query: interest over time (shared scale), interest by region, per-region share %, related topics and queries (top + rising), for a given geo/date range/category/property.

### How do I automatically compare keywords and get related queries on trends.google.com?

Ask an AI agent connected to Reduck to run reduck/trends.google.com/explore_keyword, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trends.google.com/explore_keyword

### Is there a trends.google.com API to compare keywords and get related queries?

You do not need one. "Google Trends API: compare keywords and get related queries" drives the real trends.google.com pages in a browser, so it works whether or not trends.google.com offers an API for this.

### What information do I need to provide?

Required: keywords. Optional: geo, date, category, property.

### What does it return?

It returns geo, date, keywords, byKeyword, regionShare, interestOverTime.

### Do I need to be logged in to trends.google.com?

No. It only uses pages of trends.google.com that are reachable without signing in.

### Does it change anything on trends.google.com, or only read data?

It only reads. It looks things up on trends.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/trends.google.com/explore_keyword, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trends.google.com/explore_keyword

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/trends.google.com/explore_keyword
