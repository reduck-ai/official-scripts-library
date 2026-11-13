# Search leboncoin jobs

Automatically search leboncoin jobs on leboncoin.fr. Search leboncoin's job listings ("Offres d'emploi") by free-text keyword and optional city. Results include salary, contract type, sector, experience, study level and work time when the poster provided them; those fields are null otherwise, which is common for ads with no company attached. The location is matched against leboncoin's own city list, picking the closest whole-city match; an unrecognized city is refused. Pagination is 1-based, 35 results per page; a page beyond the last is refused rather than returned as an empty result. A keyword with no match returns an empty result, not an error.

- Site: leboncoin.fr
- Address: `reduck/leboncoin.fr/search_jobs`
- Updated: 2026-11-12 (v7)
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

Search leboncoin's job listings ("Offres d'emploi") by free-text keyword and optional city. Results include salary, contract type, sector, experience, study level and work time when the poster provided them; those fields are null otherwise, which is common for ads with no company attached. The location is matched against leboncoin's own city list, picking the closest whole-city match; an unrecognized city is refused. Pagination is 1-based, 35 results per page; a page beyond the last is refused rather than returned as an empty result. A keyword with no match returns an empty result, not an error.

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

It only reads. It looks things up on leboncoin.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/leboncoin.fr/search_jobs
