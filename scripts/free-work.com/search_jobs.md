# Search Free-Work jobs

Automatically search Free-Work jobs on free-work.com. Searches job listings on free-work.com (IT/freelance), usable without logging in. `query` is a free-text keyword; `location` is a free-text city, resolved to the closest match — unresolved locations throw explicitly rather than silently searching everywhere. Defaults to searching all of France when no location is given. Returns title, full description, company, contract types, experience level, remote work, salaries (daily/annual), currency, skills, publish date, and URL. 1-based pagination, 16 results per page. One thing to check: requesting a page beyond the real number of pages doesn't return an empty result — it silently repeats the first page — so verify against `totalItems` before trusting a high page number.

- Site: free-work.com
- Address: `reduck/free-work.com/search_jobs`
- Updated: 2026-08-14 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/free-work.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/free-work.com/search_jobs
```

## Input

- `page` (integer, optional): Page number, 1-based. Defaults to 1.
- `query` (string, optional): Free-text keyword (title, skill), e.g. "python developer", "accountant". Optional.
- `location` (string, optional): Free-text city or place, e.g. "Lyon", "Paris". Resolved via the site's autocomplete (first result kept). Optional — defaults to searching all of France.

## Output

- `jobs` (array, required)
- `page` (integer, required)
- `totalItems` (integer, required)

## FAQ

### What does "Search Free-Work jobs" do?

Searches job listings on free-work.com (IT/freelance), usable without logging in. `query` is a free-text keyword; `location` is a free-text city, resolved to the closest match — unresolved locations throw explicitly rather than silently searching everywhere. Defaults to searching all of France when no location is given. Returns title, full description, company, contract types, experience level, remote work, salaries (daily/annual), currency, skills, publish date, and URL. 1-based pagination, 16 results per page. One thing to check: requesting a page beyond the real number of pages doesn't return an empty result — it silently repeats the first page — so verify against `totalItems` before trusting a high page number.

### How do I automatically search Free-Work jobs on free-work.com?

Ask an AI agent connected to Reduck to run reduck/free-work.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/free-work.com/search_jobs

### Is there a free-work.com API to search Free-Work jobs?

You do not need one. "Search Free-Work jobs" drives the real free-work.com pages in a browser, so it works whether or not free-work.com offers an API for this.

### What information do I need to provide?

Optional: page, query, location.

### What does it return?

It returns jobs, page, totalItems.

### Do I need to be logged in to free-work.com?

No. It only uses pages of free-work.com that are reachable without signing in.

### Does it change anything on free-work.com, or only read data?

It only reads. It looks things up on free-work.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/free-work.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/free-work.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/free-work.com/search_jobs
