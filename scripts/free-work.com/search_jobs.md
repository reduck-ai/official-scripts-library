# Search Free-Work jobs

Automatically search Free-Work jobs on free-work.com. Search IT and freelance job listings on Free-Work, with no sign-in. Filter by keyword and by place, given as a location key from free-work.com/suggest_locations (all of France when none is given; the place is searched within 10 km, as on the site). Returns each job's title, description, company, contract types, experience level, remote policy, daily and annual salary ranges, skills, city, publish date and link, plus the total number of matches. 16 jobs per page; asking for a page past the last one is refused.

- Site: free-work.com
- Address: `reduck/free-work.com/search_jobs`
- Updated: 2026-11-23 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/free-work.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/free-work.com/search_jobs
```

## Input

- `page` (integer, optional): Page number, 1-based.
- `query` (string, optional): Free-text keyword (title, skill), e.g. "python developer", "accountant". Optional.
- `location` (string, optional): Free-Work location key from free-work.com/suggest_locations, e.g. "fr~auvergne-rhone-alpes~rhone~lyon". Searched within 10 km, as the site does. Optional: all of France when omitted.

## Output

- `jobs` (array, required)
- `page` (integer, required)
- `totalItems` (integer, required)

## FAQ

### What does "Search Free-Work jobs" do?

Search IT and freelance job listings on Free-Work, with no sign-in. Filter by keyword and by place, given as a location key from free-work.com/suggest_locations (all of France when none is given; the place is searched within 10 km, as on the site). Returns each job's title, description, company, contract types, experience level, remote policy, daily and annual salary ranges, skills, city, publish date and link, plus the total number of matches. 16 jobs per page; asking for a page past the last one is refused.

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
