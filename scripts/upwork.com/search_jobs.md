# Search Upwork Jobs

Automatically search Upwork Jobs on upwork.com. Search Upwork's public job board by free-text query, one results page at a time (10 jobs per page; pass page for the next ones; sort by relevance or recency). Returns structured job cards (title, description, budget, skills, experience level, posting date) and the total match count. Upwork's other filters are not applied. A query with no match returns an empty list. Client details stay empty for visitors who are not signed in. When Upwork shows its login wall instead of results, the run fails with an error that says so.

- Site: upwork.com
- Address: `reduck/upwork.com/search_jobs`
- Updated: 2026-10-22 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/upwork.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/upwork.com/search_jobs
```

## Input

- `query` (string, required): Free-text search query, e.g. "web scraping lead generation" — same text you'd type in Upwork's job search box.
- `page` (integer, optional): 1-based results page (10 jobs per page).
- `sort` (string, optional): "relevance" (Upwork's best-match ranking) or "recency" (newest posted first).

## Output

- `jobs` (array, required)
- `page` (integer, optional)
- `perPage` (integer, optional)
- `totalCount` (integer | null, optional): Total matching jobs across all pages.

## FAQ

### What does "Search Upwork Jobs" do?

Search Upwork's public job board by free-text query, one results page at a time (10 jobs per page; pass page for the next ones; sort by relevance or recency). Returns structured job cards (title, description, budget, skills, experience level, posting date) and the total match count. Upwork's other filters are not applied. A query with no match returns an empty list. Client details stay empty for visitors who are not signed in. When Upwork shows its login wall instead of results, the run fails with an error that says so.

### How do I automatically search Upwork Jobs on upwork.com?

Ask an AI agent connected to Reduck to run reduck/upwork.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/upwork.com/search_jobs

### Is there a upwork.com API to search Upwork Jobs?

You do not need one. "Search Upwork Jobs" drives the real upwork.com pages in a browser, so it works whether or not upwork.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort.

### What does it return?

It returns jobs, page, perPage, totalCount.

### Do I need to be logged in to upwork.com?

No. It only uses pages of upwork.com that are reachable without signing in.

### Does it change anything on upwork.com, or only read data?

It only reads. It looks things up on upwork.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/upwork.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/upwork.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/upwork.com/search_jobs
