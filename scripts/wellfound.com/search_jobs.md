# Search Wellfound jobs

Automatically search Wellfound jobs on wellfound.com. Search Wellfound (AngelList Talent) startup job listings by role keyword, with optional city location (omit for remote-only). Returns total, page, totalPages, and jobs (jobId, title, url, company, companyUrl, jobType, compensation, locations, remote, remoteKind, acceptedRemoteLocations, yearsExperienceMin/Max, postedAt). Unrecognized roles or locations, and pages past the last one, raise an error rather than returning unrelated results. The total can exceed the jobs returned on a page, because Wellfound shows only a few jobs per company.

- Site: wellfound.com
- Address: `reduck/wellfound.com/search_jobs`
- Updated: 2026-10-23 (v7)
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
- `total` (integer, required): Wellfound's own count of matching jobs. It can exceed the jobs listed, because the page shows only a few highlighted jobs per company.
- `totalPages` (integer, required)

## FAQ

### What does "Search Wellfound jobs" do?

Search Wellfound (AngelList Talent) startup job listings by role keyword, with optional city location (omit for remote-only). Returns total, page, totalPages, and jobs (jobId, title, url, company, companyUrl, jobType, compensation, locations, remote, remoteKind, acceptedRemoteLocations, yearsExperienceMin/Max, postedAt). Unrecognized roles or locations, and pages past the last one, raise an error rather than returning unrelated results. The total can exceed the jobs returned on a page, because Wellfound shows only a few jobs per company.

### How do I automatically search Wellfound jobs on wellfound.com?

Ask an AI agent connected to Reduck to run reduck/wellfound.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wellfound.com/search_jobs

### Is there a wellfound.com API to search Wellfound jobs?

You do not need one. "Search Wellfound jobs" drives the real wellfound.com pages in a browser, so it works whether or not wellfound.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, location.

### What does it return?

It returns jobs, page, total, totalPages.

### Do I need to be logged in to wellfound.com?

No. It only uses pages of wellfound.com that are reachable without signing in.

### Does it change anything on wellfound.com, or only read data?

It only reads. It looks things up on wellfound.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/wellfound.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wellfound.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/wellfound.com/search_jobs
