# Search HelloWork jobs

Automatically search HelloWork jobs on hellowork.com. Search HelloWork's French job listings by keyword, optional free-text location, and page (30 offers/page). Returns total and jobs (jobId, title, company, url, location, contract, remoteTag, salary, superRecruiter, postedAgo). Salary and remote-work tags are only present when the listing/employer chose to show them, so they're frequently null.

- Site: hellowork.com
- Address: `reduck/hellowork.com/search_jobs`
- Updated: 2026-08-14 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hellowork.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hellowork.com/search_jobs
```

## Input

- `query` (string, required): Free-text job search query, same as HelloWork's own search box (e.g. "data engineer").
- `page` (integer, optional): 1-based page, 30 offers per page (HelloWork's own ?p= param).
- `location` (string, optional): Free-text location (e.g. "Paris", "Lyon"). Omit to search all of France.

## Output

- `jobs` (array, required)
- `page` (integer, required)
- `total` (integer, required): Matching offer count reported by HelloWork's own results header. 0 with empty jobs[] = no matching offers (first-class outcome, not an error).

## FAQ

### What does "Search HelloWork jobs" do?

Search HelloWork's French job listings by keyword, optional free-text location, and page (30 offers/page). Returns total and jobs (jobId, title, company, url, location, contract, remoteTag, salary, superRecruiter, postedAgo). Salary and remote-work tags are only present when the listing/employer chose to show them, so they're frequently null.

### How do I automatically search HelloWork jobs on hellowork.com?

Ask an AI agent connected to Reduck to run reduck/hellowork.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hellowork.com/search_jobs

### Is there a hellowork.com API to search HelloWork jobs?

You do not need one. "Search HelloWork jobs" drives the real hellowork.com pages in a browser, so it works whether or not hellowork.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, location.

### What does it return?

It returns jobs, page, total.

### Do I need to be logged in to hellowork.com?

No. It only uses pages of hellowork.com that are reachable without signing in.

### Does it change anything on hellowork.com, or only read data?

It only reads. It looks things up on hellowork.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hellowork.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hellowork.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/hellowork.com/search_jobs
