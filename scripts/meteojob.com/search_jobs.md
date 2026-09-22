# Search Meteojob jobs

Automatically search Meteojob jobs on meteojob.com. Search Meteojob's French job listings by free-text keyword and optional free-text location. Location text is validated before being used in the search — an unrecognized location raises an error rather than silently falling back to a nationwide search. Returns total and jobs (id, title, url, company, location, contractType, jobType, telework, salary, skills, publishedAt, highlight). Pagination is 1-based (20 results per page, matching the site's own page size). An unmatched keyword returns total:0, jobs:[] — not an error. Salary is the site's own free-text display string (e.g. "50 000 € - 60 000 € par an") since offers price ranges inconsistently (annual/hourly/monthly, disclosed or not).

- Site: meteojob.com
- Address: `reduck/meteojob.com/search_jobs`
- Updated: 2026-08-14 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/meteojob.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/meteojob.com/search_jobs
```

## Input

- `page` (integer, optional): 1-based page number, 20 results per page. Defaults to 1.
- `query` (string, optional): Free-text keyword, e.g. 'developpeur'
- `location` (string, optional): Free-text city name, e.g. 'Lyon'. Omit for nationwide search.

## Output

- `jobs` (array, required)
- `total` (integer, required)

## FAQ

### What does "Search Meteojob jobs" do?

Search Meteojob's French job listings by free-text keyword and optional free-text location. Location text is validated before being used in the search — an unrecognized location raises an error rather than silently falling back to a nationwide search. Returns total and jobs (id, title, url, company, location, contractType, jobType, telework, salary, skills, publishedAt, highlight). Pagination is 1-based (20 results per page, matching the site's own page size). An unmatched keyword returns total:0, jobs:[] — not an error. Salary is the site's own free-text display string (e.g. "50 000 € - 60 000 € par an") since offers price ranges inconsistently (annual/hourly/monthly, disclosed or not).

### How do I automatically search Meteojob jobs on meteojob.com?

Ask an AI agent connected to Reduck to run reduck/meteojob.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/meteojob.com/search_jobs

### Is there a meteojob.com API to search Meteojob jobs?

You do not need one. "Search Meteojob jobs" drives the real meteojob.com pages in a browser, so it works whether or not meteojob.com offers an API for this.

### What information do I need to provide?

Optional: page, query, location.

### What does it return?

It returns jobs, total.

### Do I need to be logged in to meteojob.com?

No. It only uses pages of meteojob.com that are reachable without signing in.

### Does it change anything on meteojob.com, or only read data?

Unknown: its author has not declared whether it changes anything on meteojob.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/meteojob.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/meteojob.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/meteojob.com/search_jobs
