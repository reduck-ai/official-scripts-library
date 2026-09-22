# Search SimplyHired jobs

Automatically search SimplyHired jobs on simplyhired.com. Search SimplyHired (Indeed-owned aggregator) job listings, returning richer detail than the page cards show: title, company, location, salary, benefits, requirements, snippet, remote flag, sponsored flag, dateOnIndeed. Pagination is cursor-based (not page numbers) — pass the cursor token returned in a previous call's pageCursors to get subsequent pages. Invalid/unresolvable locations return 0 results (site's own behavior), not an error.

- Site: simplyhired.com
- Address: `reduck/simplyhired.com/search_jobs`
- Updated: 2026-08-14 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/simplyhired.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/simplyhired.com/search_jobs
```

## Input

- `query` (string, required): Keyword to search (job title, skill, company). Required, non-empty — an empty/whitespace query redirects the site to its marketing homepage instead of search results.
- `cursor` (string, optional): Opaque pagination token for a page beyond the first, taken from a previous call's pageCursors (e.g. pageCursors["2"]). Omit for page 1. Note: an invalid/garbage cursor is not rejected by the site — it silently falls back to page 1.
- `location` (string, optional): Free-text location: city/state, ZIP, or "remote". Omit for a nationwide default search. Loosely matched by the site — e.g. "México" can resolve to a US town literally named Mexico rather than being rejected.

## Output

- `jobs` (array, required)
- `query` (string, required)
- `location` (string | null, required)
- `pageCursors` (object, required): Map of page number (as string, e.g. "2", "3") to opaque cursor token, for the next several pages. Empty object if no further pages.
- `resultCount` (integer, required): Total matching jobs reported by the site for this query/location (unfiltered by pagination).
- `currentPageNumber` (integer, required)

## FAQ

### What does "Search SimplyHired jobs" do?

Search SimplyHired (Indeed-owned aggregator) job listings, returning richer detail than the page cards show: title, company, location, salary, benefits, requirements, snippet, remote flag, sponsored flag, dateOnIndeed. Pagination is cursor-based (not page numbers) — pass the cursor token returned in a previous call's pageCursors to get subsequent pages. Invalid/unresolvable locations return 0 results (site's own behavior), not an error.

### How do I automatically search SimplyHired jobs on simplyhired.com?

Ask an AI agent connected to Reduck to run reduck/simplyhired.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/simplyhired.com/search_jobs

### Is there a simplyhired.com API to search SimplyHired jobs?

You do not need one. "Search SimplyHired jobs" drives the real simplyhired.com pages in a browser, so it works whether or not simplyhired.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: cursor, location.

### What does it return?

It returns jobs, query, location, pageCursors, resultCount, currentPageNumber.

### Do I need to be logged in to simplyhired.com?

No. It only uses pages of simplyhired.com that are reachable without signing in.

### Does it change anything on simplyhired.com, or only read data?

Unknown: its author has not declared whether it changes anything on simplyhired.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/simplyhired.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/simplyhired.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/simplyhired.com/search_jobs
