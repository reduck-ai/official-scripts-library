# Search Himalayas remote jobs

Automatically search Himalayas remote jobs on himalayas.app. Search Himalayas (himalayas.app) remote job listings by a free-text description of the desired role (e.g. "python developer in france", "senior product designer, remote worldwide") — the same single natural-language box the site's own UI exposes ("Describe your ideal remote job..."). Returns total (from the site's own job counter) and jobs (title, url, company, companyUrl, postedAgo, location, salary, tags). Paginates via the site's own page param (page=1 default, 20 results/page). An unrecognized query falls back to the full unfiltered listing (~100k+ jobs) rather than returning zero results — check the returned filtered flag (false when this fallback happened) rather than trusting total alone.

- Site: himalayas.app
- Address: `reduck/himalayas.app/search_jobs`
- Updated: 2026-09-25 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/himalayas.app/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/himalayas.app/search_jobs
```

## Input

- `query` (string, required): Free-text description of the desired role, e.g. "python developer in france". Must be non-empty (whitespace-only also rejected) — the site's search never fires otherwise.
- `page` (integer, optional): 1-based page number. Default 1. A page past the last one available returns filtered:null, jobs:[] (Himalayas renders a 404 there instead of an empty results page).

## Output

- `jobs` (array, required)
- `filtered` (boolean | null, required): False when Himalayas' AI parser could not resolve the query and fell back to the full unfiltered job catalogue. Null when the requested page is past the last one available (Himalayas renders a generic 404 rather than an empty results page in that case).
- `total` (number | null, optional)

## FAQ

### What does "Search Himalayas remote jobs" do?

Search Himalayas (himalayas.app) remote job listings by a free-text description of the desired role (e.g. "python developer in france", "senior product designer, remote worldwide") — the same single natural-language box the site's own UI exposes ("Describe your ideal remote job..."). Returns total (from the site's own job counter) and jobs (title, url, company, companyUrl, postedAgo, location, salary, tags). Paginates via the site's own page param (page=1 default, 20 results/page). An unrecognized query falls back to the full unfiltered listing (~100k+ jobs) rather than returning zero results — check the returned filtered flag (false when this fallback happened) rather than trusting total alone.

### How do I automatically search Himalayas remote jobs on himalayas.app?

Ask an AI agent connected to Reduck to run reduck/himalayas.app/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/himalayas.app/search_jobs

### Is there a himalayas.app API to search Himalayas remote jobs?

You do not need one. "Search Himalayas remote jobs" drives the real himalayas.app pages in a browser, so it works whether or not himalayas.app offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns jobs, total, filtered.

### Do I need to be logged in to himalayas.app?

No. It only uses pages of himalayas.app that are reachable without signing in.

### Does it change anything on himalayas.app, or only read data?

It only reads. It looks things up on himalayas.app and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/himalayas.app/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/himalayas.app/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/himalayas.app/search_jobs
