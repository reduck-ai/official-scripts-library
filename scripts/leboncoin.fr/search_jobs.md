# Search leboncoin jobs

Automatically search leboncoin jobs on leboncoin.fr. Search leboncoin's "Offres d'emploi" (job listings) category by free-text keyword and optional free-text city location. Reads the search page's own richer underlying data rather than the visible cards, so results include salary, contract type, sector, experience, study level, and work time when the poster provided them (fields are null otherwise, which is common for private-seller ads with no company attached). Location text is matched against leboncoin's own city list, picking the closest whole-city match; an unrecognized location throws. Pagination is 1-based, 35 results per page. An unmatched keyword returns a clean empty result rather than an error. One known limitation: requesting a page beyond the search's real page count is detected and reported as an explicit out-of-range error, rather than the misleading empty result leboncoin's own site would otherwise show.

- Site: leboncoin.fr
- Address: `reduck/leboncoin.fr/search_jobs`
- Updated: 2026-08-14 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leboncoin.fr/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/search_jobs
```

## Input

- `page` (integer, optional): 1-based page number, 35 results per page. Defaults to 1.
- `query` (string, optional): Free-text keyword, e.g. 'developpeur'
- `location` (string, optional): Free-text city name, e.g. 'Lyon'. Omit for nationwide search.

## Output

- `jobs` (array, required)
- `total` (integer, required)

## FAQ

### What does "Search leboncoin jobs" do?

Search leboncoin's "Offres d'emploi" (job listings) category by free-text keyword and optional free-text city location. Reads the search page's own richer underlying data rather than the visible cards, so results include salary, contract type, sector, experience, study level, and work time when the poster provided them (fields are null otherwise, which is common for private-seller ads with no company attached). Location text is matched against leboncoin's own city list, picking the closest whole-city match; an unrecognized location throws. Pagination is 1-based, 35 results per page. An unmatched keyword returns a clean empty result rather than an error. One known limitation: requesting a page beyond the search's real page count is detected and reported as an explicit out-of-range error, rather than the misleading empty result leboncoin's own site would otherwise show.

### How do I automatically search leboncoin jobs on leboncoin.fr?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/search_jobs

### Is there a leboncoin.fr API to search leboncoin jobs?

You do not need one. "Search leboncoin jobs" drives the real leboncoin.fr pages in a browser, so it works whether or not leboncoin.fr offers an API for this.

### What information do I need to provide?

Optional: page, query, location.

### What does it return?

It returns jobs, total.

### Do I need to be logged in to leboncoin.fr?

No. It only uses pages of leboncoin.fr that are reachable without signing in.

### Does it change anything on leboncoin.fr, or only read data?

Unknown: its author has not declared whether it changes anything on leboncoin.fr, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/leboncoin.fr/search_jobs
