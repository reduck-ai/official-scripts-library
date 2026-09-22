# Dealroom: Search Companies

Automatically search Companies on dealroom.co. Search Dealroom's company database by technology, industry, HQ location and launch year. Returns each match's tagline, growth stage, funding, valuation, industries and HQ. Free/registered Dealroom accounts see a small number of results per search (observed cap: 6), sorted by Dealroom's own ranking, and are subject to Dealroom's daily search-view limit.

- Site: dealroom.co
- Address: `reduck/dealroom.co/search_companies`
- Updated: 2026-09-09 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dealroom.co/search_companies`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dealroom.co/search_companies
```

## Input

- `limit` (integer, optional): Max companies to return (default 10; Dealroom returns only a handful of raw results per search regardless of this value on free/registered accounts, observed cap: 6).
- `industry` (string, optional): Industry keyword to filter by, matched against Dealroom's own industry tags, e.g. "fintech", "health" (not "healthtech" — Dealroom's tag for that space is "health").
- `technology` (string, optional): Technology keyword to filter by, e.g. "artificial intelligence", "blockchain" (matched against Dealroom's technology tags).
- `locationSlug` (string, optional): Dealroom HQ location slug, e.g. "france", "united_states", "berlin", "san_francisco". Must be Dealroom's own slug format (lowercase, underscores for spaces), not a free-text place name.
- `launchYearMax` (integer, optional): Only include companies founded in or before this year.
- `launchYearMin` (integer, optional): Only include companies founded in or after this year.

## Output

- `items` (array, required)
- `total` (integer | null, optional): Total matching companies reported by Dealroom for this filter combination.

## FAQ

### What does "Dealroom: Search Companies" do?

Search Dealroom's company database by technology, industry, HQ location and launch year. Returns each match's tagline, growth stage, funding, valuation, industries and HQ. Free/registered Dealroom accounts see a small number of results per search (observed cap: 6), sorted by Dealroom's own ranking, and are subject to Dealroom's daily search-view limit.

### How do I automatically search Companies on dealroom.co?

Ask an AI agent connected to Reduck to run reduck/dealroom.co/search_companies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dealroom.co/search_companies

### Is there a dealroom.co API to search Companies?

You do not need one. "Dealroom: Search Companies" drives the real dealroom.co pages in a browser, so it works whether or not dealroom.co offers an API for this.

### What information do I need to provide?

Optional: limit, industry, technology, locationSlug, launchYearMax, launchYearMin.

### What does it return?

It returns items, total.

### Do I need to be logged in to dealroom.co?

No. It only uses pages of dealroom.co that are reachable without signing in.

### Does it change anything on dealroom.co, or only read data?

It only reads. It looks things up on dealroom.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dealroom.co/search_companies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dealroom.co/search_companies

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dealroom.co/search_companies
