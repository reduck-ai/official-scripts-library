# Search Indeed jobs

Automatically search Indeed jobs on indeed.com. Search Indeed's public job listings by keyword, optional free-text location and country site (e.g. "fr" for fr.indeed.com, default "us"). Returns total, page, outOfCountry, and jobs (jobKey, title, company, location, salary, jobTypes, remote, sponsored, postedAgo, url). Anonymous search only reliably supports page=1 — Indeed gates further pages behind a sign-in wall, and the script throws loudly if that gate appears. total/results are only meaningful for the requested location when outOfCountry is false; indeed.com (US) treats non-US locations as out-of-country and returns unrelated jobs.

- Site: indeed.com
- Address: `reduck/indeed.com/search_jobs`
- Updated: 2026-09-17 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/indeed.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/indeed.com/search_jobs
```

## Input

- `query` (string, required): Free-text job search query, same as Indeed's search box (e.g. "data engineer"). Must be non-empty — an empty query redirects Indeed to its homepage instead of a results page.
- `page` (integer, optional): 1-based page. Only page=1 is reliably supported anonymously — Indeed shows a sign-in wall for further pages, which the script surfaces as a thrown error.
- `sortBy` (string, optional): Sort order. Default: relevance (Indeed's own default).
- `country` (string, optional): Indeed country site to search, as its subdomain code (e.g. "us", "fr", "de", "uk", "ca"). Lowercased; "us" maps to www.indeed.com, others to "<country>.indeed.com".
- `location` (string, optional): Free-text location (e.g. "Paris", "Berlin"). Must match the chosen country site or Indeed marks the result outOfCountry and returns unrelated jobs.

## Output

- `jobs` (array, required)
- `page` (integer, required)
- `total` (integer, required): Matching job count reported by Indeed for this query/location. Not meaningful when outOfCountry is true (Indeed falls back to a broad, location-agnostic count).
- `outOfCountry` (boolean, required): True when Indeed treated the requested location as outside the chosen country site — total and jobs then reflect a fallback, not the requested location.

## FAQ

### What does "Search Indeed jobs" do?

Search Indeed's public job listings by keyword, optional free-text location and country site (e.g. "fr" for fr.indeed.com, default "us"). Returns total, page, outOfCountry, and jobs (jobKey, title, company, location, salary, jobTypes, remote, sponsored, postedAgo, url). Anonymous search only reliably supports page=1 — Indeed gates further pages behind a sign-in wall, and the script throws loudly if that gate appears. total/results are only meaningful for the requested location when outOfCountry is false; indeed.com (US) treats non-US locations as out-of-country and returns unrelated jobs.

### How do I automatically search Indeed jobs on indeed.com?

Ask an AI agent connected to Reduck to run reduck/indeed.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/indeed.com/search_jobs

### Is there a indeed.com API to search Indeed jobs?

You do not need one. "Search Indeed jobs" drives the real indeed.com pages in a browser, so it works whether or not indeed.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sortBy, country, location.

### What does it return?

It returns jobs, page, total, outOfCountry.

### Do I need to be logged in to indeed.com?

No. It only uses pages of indeed.com that are reachable without signing in.

### Does it change anything on indeed.com, or only read data?

Unknown: its author has not declared whether it changes anything on indeed.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/indeed.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/indeed.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/indeed.com/search_jobs
