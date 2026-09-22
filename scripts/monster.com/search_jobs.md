# Search Monster jobs

Automatically search Monster jobs on monster.com. Search Monster's US job listings by free-text keyword and optional free-text location (city/state, e.g. "Austin, TX"; omit for a nationwide/remote search). Returns total (jobs on this page, max 18), estimatedTotal (Monster's own broader estimate across the full index) and jobs (jobId, title, company, location, remote, salary, currency, datePosted, url, applyUrl). Monster always searches scoped to the US regardless of the location text typed — this mirrors monster.com's own site behavior (it is a US-market board); a non-US location (e.g. "Paris, France") is not rejected — Monster's own geocoding can silently match a same-named US place instead (e.g. resolving to Paris, Maine) and return results for that place. Paginates via page (1, 2, ...; 18 results/page); results may repeat sponsored/promoted listings across pages, matching the site's own behavior. A keyword with no matches returns total:0, jobs:[] — not an error.

- Site: monster.com
- Address: `reduck/monster.com/search_jobs`
- Updated: 2026-08-30 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/monster.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/monster.com/search_jobs
```

## Input

- `query` (string, required): Free-text keyword search, e.g. "software engineer"
- `page` (integer, optional): 1-based page number, 18 results per page. Defaults to 1.
- `where` (string, optional): Free-text US location, e.g. "Austin, TX" or "remote". Omit for a nationwide search.

## Output

- `jobs` (array, required)
- `total` (integer, required)
- `estimatedTotal` (integer, required)

## FAQ

### What does "Search Monster jobs" do?

Search Monster's US job listings by free-text keyword and optional free-text location (city/state, e.g. "Austin, TX"; omit for a nationwide/remote search). Returns total (jobs on this page, max 18), estimatedTotal (Monster's own broader estimate across the full index) and jobs (jobId, title, company, location, remote, salary, currency, datePosted, url, applyUrl). Monster always searches scoped to the US regardless of the location text typed — this mirrors monster.com's own site behavior (it is a US-market board); a non-US location (e.g. "Paris, France") is not rejected — Monster's own geocoding can silently match a same-named US place instead (e.g. resolving to Paris, Maine) and return results for that place. Paginates via page (1, 2, ...; 18 results/page); results may repeat sponsored/promoted listings across pages, matching the site's own behavior. A keyword with no matches returns total:0, jobs:[] — not an error.

### How do I automatically search Monster jobs on monster.com?

Ask an AI agent connected to Reduck to run reduck/monster.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/monster.com/search_jobs

### Is there a monster.com API to search Monster jobs?

You do not need one. "Search Monster jobs" drives the real monster.com pages in a browser, so it works whether or not monster.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, where.

### What does it return?

It returns jobs, total, estimatedTotal.

### Do I need to be logged in to monster.com?

No. It only uses pages of monster.com that are reachable without signing in.

### Does it change anything on monster.com, or only read data?

It only reads. It looks things up on monster.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/monster.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/monster.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/monster.com/search_jobs
