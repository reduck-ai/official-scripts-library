# Search Built In jobs

Automatically search Built In jobs on builtin.com. Search Built In (builtin.com) tech/startup job listings by free-text keyword and optional free-text location (city). Returns id, title, url, company, companyUrl, postedAgo, remoteType (Remote/Hybrid/In-Office wording as shown), locations (array — cards with several offices list each one), salary (raw site text, e.g. "180K-201K Annually" — not split into min/max since the site itself only shows a range string, sometimes absent when undisclosed), seniority, industries (array), description, topSkills (array). Paginates via the site's own page param (page=1 default, 25 results/page); the reported last page reflects the true total, not just the current page's count. A query/location with no matches returns jobs:[] — not an error.

- Site: builtin.com
- Address: `reduck/builtin.com/search_jobs`
- Updated: 2026-08-17 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/builtin.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/builtin.com/search_jobs
```

## Input

- `query` (string, required): Free-text keyword, e.g. "software engineer"
- `page` (integer, optional): 1-based page number. Default 1.
- `location` (string, optional): Free-text city, e.g. "austin". Omit for Built In's default (geo-resolved) scope.

## Output

- `jobs` (array, required)

## FAQ

### What does "Search Built In jobs" do?

Search Built In (builtin.com) tech/startup job listings by free-text keyword and optional free-text location (city). Returns id, title, url, company, companyUrl, postedAgo, remoteType (Remote/Hybrid/In-Office wording as shown), locations (array — cards with several offices list each one), salary (raw site text, e.g. "180K-201K Annually" — not split into min/max since the site itself only shows a range string, sometimes absent when undisclosed), seniority, industries (array), description, topSkills (array). Paginates via the site's own page param (page=1 default, 25 results/page); the reported last page reflects the true total, not just the current page's count. A query/location with no matches returns jobs:[] — not an error.

### How do I automatically search Built In jobs on builtin.com?

Ask an AI agent connected to Reduck to run reduck/builtin.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/builtin.com/search_jobs

### Is there a builtin.com API to search Built In jobs?

You do not need one. "Search Built In jobs" drives the real builtin.com pages in a browser, so it works whether or not builtin.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, location.

### What does it return?

It returns jobs.

### Do I need to be logged in to builtin.com?

No. It only uses pages of builtin.com that are reachable without signing in.

### Does it change anything on builtin.com, or only read data?

It only reads. It looks things up on builtin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/builtin.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/builtin.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/builtin.com/search_jobs
