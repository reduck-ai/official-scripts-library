# Search talent.com jobs

Automatically search talent.com jobs on talent.com. Search talent.com's aggregated job listings by keyword and optional city or region. Returns each job's title, company, location, salary range, remote flag, job type, posting date and description, about 18 to 20 per page. There is no total count, so page until an empty list comes back. Location text is matched loosely, the same as the site's own search box (for example "paris" can resolve to Paris, Texas). A query with no matches returns an empty list, not an error.

- Site: talent.com
- Address: `reduck/talent.com/search_jobs`
- Updated: 2026-10-29 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/talent.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/talent.com/search_jobs
```

## Input

- `query` (string, required): Free-text keyword, e.g. "python developer"
- `page` (integer, optional): 1-based page number.
- `location` (string, optional): Free-text city/region, e.g. "new york". Omit for talent.com's default (geo-resolved) scope.

## Output

- `jobs` (array, required)

## FAQ

### What does "Search talent.com jobs" do?

Search talent.com's aggregated job listings by keyword and optional city or region. Returns each job's title, company, location, salary range, remote flag, job type, posting date and description, about 18 to 20 per page. There is no total count, so page until an empty list comes back. Location text is matched loosely, the same as the site's own search box (for example "paris" can resolve to Paris, Texas). A query with no matches returns an empty list, not an error.

### How do I automatically search talent.com jobs on talent.com?

Ask an AI agent connected to Reduck to run reduck/talent.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/talent.com/search_jobs

### Is there a talent.com API to search talent.com jobs?

You do not need one. "Search talent.com jobs" drives the real talent.com pages in a browser, so it works whether or not talent.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, location.

### What does it return?

It returns jobs.

### Do I need to be logged in to talent.com?

No. It only uses pages of talent.com that are reachable without signing in.

### Does it change anything on talent.com, or only read data?

It only reads. It looks things up on talent.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/talent.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/talent.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/talent.com/search_jobs
