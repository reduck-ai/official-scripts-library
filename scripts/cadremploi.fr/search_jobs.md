# Search Cadremploi jobs

Automatically search Cadremploi jobs on cadremploi.fr. Search Cadremploi (French executive/manager job board) by free-text keyword and optional free-text city location. Location text is resolved via Cadremploi's own location suggestions, picking the first city-level match — same as picking the top "Villes" suggestion in the UI; a location with no city-level match throws (department/region-only matches, e.g. a region name with no matching city, are not supported by this script). Passing raw location text through without this resolution step silently falls back to a nationwide search on Cadremploi's side, which is why resolution is mandatory here. Cadremploi itself returns three tiers per search — exact city matches, matches in the surrounding area, and an "expanded" broader-radius fallback — all rendered together as one list with no visual divider; this script preserves that distinction via each job's matchType field rather than picking one arbitrarily. total is the grand total across all three tiers (also the number returned with no location filter, i.e. nationwide). Optional radius (km) mirrors the site's own distance-around-city filter; optional page paginates in fixed batches of 50 (site's own page size), matching the site's own ?page= param. An unmatched keyword returns total:0, jobs:[] — not an error.

- Site: cadremploi.fr
- Address: `reduck/cadremploi.fr/search_jobs`
- Updated: 2026-08-17 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cadremploi.fr/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cadremploi.fr/search_jobs
```

## Input

- `page` (integer, optional): 1-based page number, 50 results per page. Defaults to 1.
- `query` (string, optional): Free-text keyword, e.g. "developpeur". Omit to browse all listings (optionally filtered by location).
- `where` (string, optional): Free-text French city, e.g. "Paris" or "Lyon". Resolved via Cadremploi's own location-suggestions API; throws if no city-level match exists. Omit for a nationwide search.
- `radius` (integer, optional): Search radius in km around the resolved city. Site default is 20 when a city is given.

## Output

- `jobs` (array, required)
- `total` (integer, required)

## FAQ

### What does "Search Cadremploi jobs" do?

Search Cadremploi (French executive/manager job board) by free-text keyword and optional free-text city location. Location text is resolved via Cadremploi's own location suggestions, picking the first city-level match — same as picking the top "Villes" suggestion in the UI; a location with no city-level match throws (department/region-only matches, e.g. a region name with no matching city, are not supported by this script). Passing raw location text through without this resolution step silently falls back to a nationwide search on Cadremploi's side, which is why resolution is mandatory here. Cadremploi itself returns three tiers per search — exact city matches, matches in the surrounding area, and an "expanded" broader-radius fallback — all rendered together as one list with no visual divider; this script preserves that distinction via each job's matchType field rather than picking one arbitrarily. total is the grand total across all three tiers (also the number returned with no location filter, i.e. nationwide). Optional radius (km) mirrors the site's own distance-around-city filter; optional page paginates in fixed batches of 50 (site's own page size), matching the site's own ?page= param. An unmatched keyword returns total:0, jobs:[] — not an error.

### How do I automatically search Cadremploi jobs on cadremploi.fr?

Ask an AI agent connected to Reduck to run reduck/cadremploi.fr/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cadremploi.fr/search_jobs

### Is there a cadremploi.fr API to search Cadremploi jobs?

You do not need one. "Search Cadremploi jobs" drives the real cadremploi.fr pages in a browser, so it works whether or not cadremploi.fr offers an API for this.

### What information do I need to provide?

Optional: page, query, where, radius.

### What does it return?

It returns jobs, total.

### Do I need to be logged in to cadremploi.fr?

No. It only uses pages of cadremploi.fr that are reachable without signing in.

### Does it change anything on cadremploi.fr, or only read data?

It only reads. It looks things up on cadremploi.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cadremploi.fr/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cadremploi.fr/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cadremploi.fr/search_jobs
