# Search Jooble jobs

Automatically search Jooble jobs on jooble.org. Searches job listings on jooble.org (global/US, English UI) by driving the site's own search form (keyword + city) and reading the results it returns. Dismisses the cookie-consent banner if present. Pagination beyond the first page is loaded via progressive scroll, matching the site's own infinite-scroll behavior. One thing to be aware of: Jooble is sensitive to request rate and can temporarily block rapid repeated searches within a short window; if a search fails, space out retries rather than repeating it immediately.

- Site: jooble.org
- Address: `reduck/jooble.org/search_jobs`
- Updated: 2026-08-14 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/jooble.org/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/jooble.org/search_jobs
```

## Input

- `query` (string, required): Search keyword (job, skill, job title), e.g. "accountant", "python developer".
- `page` (integer, optional): Page number, 1-based. Defaults to 1 (first 20 results). Later pages are loaded via progressive scroll, as on the site.
- `location` (string, optional): Free-text city or region, e.g. "Lyon", "Paris". Optional — defaults to searching all of France.

## Output

- `jobs` (array, required)
- `page` (integer, required)
- `jobsAmount` (integer, required): Number of listings matching the current filter (keyword + location)
- `totalJobsAmount` (integer, required): Total number of listings across all of Jooble France
- `region` (string | null, optional)

## FAQ

### What does "Search Jooble jobs" do?

Searches job listings on jooble.org (global/US, English UI) by driving the site's own search form (keyword + city) and reading the results it returns. Dismisses the cookie-consent banner if present. Pagination beyond the first page is loaded via progressive scroll, matching the site's own infinite-scroll behavior. One thing to be aware of: Jooble is sensitive to request rate and can temporarily block rapid repeated searches within a short window; if a search fails, space out retries rather than repeating it immediately.

### How do I automatically search Jooble jobs on jooble.org?

Ask an AI agent connected to Reduck to run reduck/jooble.org/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jooble.org/search_jobs

### Is there a jooble.org API to search Jooble jobs?

You do not need one. "Search Jooble jobs" drives the real jooble.org pages in a browser, so it works whether or not jooble.org offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, location.

### What does it return?

It returns jobs, page, region, jobsAmount, totalJobsAmount.

### Do I need to be logged in to jooble.org?

No. It only uses pages of jooble.org that are reachable without signing in.

### Does it change anything on jooble.org, or only read data?

It only reads. It looks things up on jooble.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/jooble.org/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jooble.org/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/jooble.org/search_jobs
