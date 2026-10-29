# Search RemoteOK jobs

Automatically search RemoteOK jobs on remoteok.com. Search all live RemoteOK job postings with the same fuzzy full-text match as the site's search box, or omit the query for the most recent postings. Returns up to 50 jobs per page with title, company, tags, location, date and salary; page with offset. Salary is null when the employer gave none.

- Site: remoteok.com
- Address: `reduck/remoteok.com/search_jobs`
- Updated: 2026-10-28 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/remoteok.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/remoteok.com/search_jobs
```

## Input

- `query` (string, optional): Full-text search, the same fuzzy match as the site's search box, across all live RemoteOK postings. Omit for the unfiltered recent-postings feed.
- `offset` (integer, optional): Number of jobs to skip; pages hold up to 50 jobs. Increase by 50 until a page returns fewer than 50. The feed moves, so dedupe by id when merging pages fetched at different times.

## Output

- `jobs` (array, required)

## FAQ

### What does "Search RemoteOK jobs" do?

Search all live RemoteOK job postings with the same fuzzy full-text match as the site's search box, or omit the query for the most recent postings. Returns up to 50 jobs per page with title, company, tags, location, date and salary; page with offset. Salary is null when the employer gave none.

### How do I automatically search RemoteOK jobs on remoteok.com?

Ask an AI agent connected to Reduck to run reduck/remoteok.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/remoteok.com/search_jobs

### Is there a remoteok.com API to search RemoteOK jobs?

You do not need one. "Search RemoteOK jobs" drives the real remoteok.com pages in a browser, so it works whether or not remoteok.com offers an API for this.

### What information do I need to provide?

Optional: query, offset.

### What does it return?

It returns jobs.

### Do I need to be logged in to remoteok.com?

No. It only uses pages of remoteok.com that are reachable without signing in.

### Does it change anything on remoteok.com, or only read data?

Unknown: its author has not declared whether it changes anything on remoteok.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/remoteok.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/remoteok.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/remoteok.com/search_jobs
