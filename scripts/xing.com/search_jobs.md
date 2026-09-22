# Search XING Jobs

Automatically search XING Jobs on xing.com. Search XING Jobs (German-speaking professional network) by free-text keyword and optional free-text location (city), via XING's own query-string job search rather than its natural-language "Tell the XING AI about the job you want" search box. Returns total (site's own counter, capped and displayed as "999+" for very broad queries - not an exact count past that point) and jobs (jobId, title, company, location, moreLocations, employmentType, salary, urgentlyHiring, postedAgo, postedAt, easyApply, sponsored, url). A few things to know: an unmatched keyword and/or an unresolvable location do not reliably produce a true zero-result signal via the total counter - XING can silently fall back to an unfiltered (or location-only-filtered) broad result set while still reporting a normal-looking "N jobs found", so total/location alone should not be trusted to detect a true no-match; an unresolvable location is silently dropped server-side to a nationwide search, same pattern as some other job boards. Pagination is reliable at its true boundary, though: once a page number goes past the site's actual result count, this script returns jobs:[] for a genuine "no matching jobs" state, ignoring that page's unrelated "jobs we found elsewhere" suggestions - those reuse the same card markup as real results but are not matches. Going further still (a page number far beyond any reasonable range) throws an explicit error instead of hanging. Some result cards are third-party syndicated listings (e.g. via jobware.de, jooble.org, meinestadt.de, heyjobs.co) rather than native XING job pages - these have sponsored:true, url pointing off-site, and jobId:null (no internal XING job id exists for them), which is the site's own real behavior, not a missing field. Pagination is 1-based via the site's own page param (page=1 default, 20 results/page).

- Site: xing.com
- Address: `reduck/xing.com/search_jobs`
- Updated: 2026-08-14 (v5)
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
- `totalRaw` (string | null, required): Site's own result counter text, e.g. "580 jobs found"/"580 Jobs gefunden" or "999+" variants (capped, not exact, past 999). Is instead the literal no-match heading (English or German) when jobs is empty because the page/filters are past the site's real result count (a true empty state, distinct from the keyword/location fallback quirk described in the script's description).

## FAQ

### What does "Search XING Jobs" do?

Search XING Jobs (German-speaking professional network) by free-text keyword and optional free-text location (city), via XING's own query-string job search rather than its natural-language "Tell the XING AI about the job you want" search box. Returns total (site's own counter, capped and displayed as "999+" for very broad queries - not an exact count past that point) and jobs (jobId, title, company, location, moreLocations, employmentType, salary, urgentlyHiring, postedAgo, postedAt, easyApply, sponsored, url). A few things to know: an unmatched keyword and/or an unresolvable location do not reliably produce a true zero-result signal via the total counter - XING can silently fall back to an unfiltered (or location-only-filtered) broad result set while still reporting a normal-looking "N jobs found", so total/location alone should not be trusted to detect a true no-match; an unresolvable location is silently dropped server-side to a nationwide search, same pattern as some other job boards. Pagination is reliable at its true boundary, though: once a page number goes past the site's actual result count, this script returns jobs:[] for a genuine "no matching jobs" state, ignoring that page's unrelated "jobs we found elsewhere" suggestions - those reuse the same card markup as real results but are not matches. Going further still (a page number far beyond any reasonable range) throws an explicit error instead of hanging. Some result cards are third-party syndicated listings (e.g. via jobware.de, jooble.org, meinestadt.de, heyjobs.co) rather than native XING job pages - these have sponsored:true, url pointing off-site, and jobId:null (no internal XING job id exists for them), which is the site's own real behavior, not a missing field. Pagination is 1-based via the site's own page param (page=1 default, 20 results/page).

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
