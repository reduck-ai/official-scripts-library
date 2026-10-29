# Search Cadremploi jobs

Automatically search Cadremploi jobs on cadremploi.fr. Search Cadremploi (French executive and manager job board) by keyword and optional French city, with an optional radius in km and paging (30 per page). A city Cadremploi does not recognize fails with an error; regions and departments are not supported. Results come in Cadremploi's groups: exact matches, matches around the city, a wider fallback and related offers; each job's matchType says which. total counts all of them. An unmatched keyword returns total 0 and an empty list, not an error.

- Site: cadremploi.fr
- Address: `reduck/cadremploi.fr/search_jobs`
- Updated: 2026-10-28 (v3)
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

Search Cadremploi (French executive and manager job board) by keyword and optional French city, with an optional radius in km and paging (30 per page). A city Cadremploi does not recognize fails with an error; regions and departments are not supported. Results come in Cadremploi's groups: exact matches, matches around the city, a wider fallback and related offers; each job's matchType says which. total counts all of them. An unmatched keyword returns total 0 and an empty list, not an error.

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
