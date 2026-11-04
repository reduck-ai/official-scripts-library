# Search XING Jobs

Automatically search XING Jobs on xing.com. Search Xing Jobs by keyword and optional city, 20 jobs per page. Returns each job's id, title, company, city (plus how many other cities), employment type, salary range when the posting has one, when it was posted, whether you apply on Xing itself, whether the listing comes from a third-party site, and its link. Xing's search is semantic: a keyword with no exact match still returns related jobs, and an unknown city is ignored and searched nationwide, so an empty list is rare. The result count is usually not given.

- Site: xing.com
- Address: `reduck/xing.com/search_jobs`
- Updated: 2026-11-03 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/xing.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/xing.com/search_jobs
```

## Input

- `query` (string, required): Free-text keyword, e.g. job title or skill (e.g. "software developer")
- `page` (integer, optional): 1-based page number, 20 results per page
- `location` (string, optional): Optional free-text city/location to filter by (e.g. "Berlin"). Omit for a nationwide/remote search.

## Output

- `jobs` (array, required)
- `totalRaw` (string | null, required): Result count from the site's data; null when the site gives no count (the default semantic search reports none)

## FAQ

### What does "Search XING Jobs" do?

Search Xing Jobs by keyword and optional city, 20 jobs per page. Returns each job's id, title, company, city (plus how many other cities), employment type, salary range when the posting has one, when it was posted, whether you apply on Xing itself, whether the listing comes from a third-party site, and its link. Xing's search is semantic: a keyword with no exact match still returns related jobs, and an unknown city is ignored and searched nationwide, so an empty list is rare. The result count is usually not given.

### How do I automatically search XING Jobs on xing.com?

Ask an AI agent connected to Reduck to run reduck/xing.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/xing.com/search_jobs

### Is there a xing.com API to search XING Jobs?

You do not need one. "Search XING Jobs" drives the real xing.com pages in a browser, so it works whether or not xing.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, location.

### What does it return?

It returns jobs, totalRaw.

### Do I need to be logged in to xing.com?

No. It only uses pages of xing.com that are reachable without signing in.

### Does it change anything on xing.com, or only read data?

It only reads. It looks things up on xing.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/xing.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/xing.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/xing.com/search_jobs
