# Search Wellfound jobs

Automatically search Wellfound jobs on wellfound.com. Search Wellfound (AngelList Talent) startup job listings by role keyword, with optional city location (omit for remote-only). Returns total, page, totalPages, complete, and jobs (jobId, title, url, company, companyUrl, jobType, compensation, locations, remote, remoteKind, acceptedRemoteLocations, yearsExperienceMin/Max, postedAt). Wellfound shows only a few jobs per company, so its total can exceed the jobs it lists: complete is true only when every counted job is listed, and false when some were left out or the results span several pages. The listed jobs are each matching company's highlighted ones and can include other roles. Unrecognized roles or locations, and pages past the last one, raise an error rather than returning unrelated results.

- Site: wellfound.com
- Address: `reduck/wellfound.com/search_jobs`
- Updated: 2026-10-28 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/wellfound.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/wellfound.com/search_jobs
```

## Input

- `query` (string, required): Free-text job role/title (e.g. "data engineer", "product manager"). Slugified and matched against Wellfound's own role taxonomy — unrecognized roles cause the script to throw rather than silently return unrelated jobs.
- `page` (integer, optional): 1-based page, per Wellfound's own pagination (?page=N).
- `location` (string, optional): Free-text city (e.g. "Paris", "San Francisco"). Omit to search remote-only listings. Slugified and matched against Wellfound's own location taxonomy; unrecognized locations cause the script to throw.

## Output

- `jobs` (array, required)
- `page` (integer, required)
- `total` (integer, required): Wellfound's own count of matching jobs across all pages. It can exceed the jobs listed, because a results page shows at most a few jobs per company.
- `complete` (boolean, required): True when every job Wellfound counts is listed across the pages, i.e. the page left none out. False when Wellfound counted more jobs than its pages list (it shows only a few per company); the rest are on each company's own page.
- `totalPages` (integer, required)

## FAQ

### What does "Search Wellfound jobs" do?

Search Wellfound (AngelList Talent) startup job listings by role keyword, with optional city location (omit for remote-only). Returns total, page, totalPages, complete, and jobs (jobId, title, url, company, companyUrl, jobType, compensation, locations, remote, remoteKind, acceptedRemoteLocations, yearsExperienceMin/Max, postedAt). Wellfound shows only a few jobs per company, so its total can exceed the jobs it lists: complete is true only when every counted job is listed, and false when some were left out or the results span several pages. The listed jobs are each matching company's highlighted ones and can include other roles. Unrecognized roles or locations, and pages past the last one, raise an error rather than returning unrelated results.

### How do I automatically search Wellfound jobs on wellfound.com?

Ask an AI agent connected to Reduck to run reduck/wellfound.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wellfound.com/search_jobs

### Is there a wellfound.com API to search Wellfound jobs?

You do not need one. "Search Wellfound jobs" drives the real wellfound.com pages in a browser, so it works whether or not wellfound.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, location.

### What does it return?

It returns jobs, page, total, complete, totalPages.

### Do I need to be logged in to wellfound.com?

No. It only uses pages of wellfound.com that are reachable without signing in.

### Does it change anything on wellfound.com, or only read data?

It only reads. It looks things up on wellfound.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/wellfound.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wellfound.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/wellfound.com/search_jobs
