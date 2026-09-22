# Get LinkedIn company jobs

Automatically get LinkedIn company jobs on linkedin.com. Get a LinkedIn company's open job postings by numeric companyId, worldwide by default, paginated (25/page). Returns total, page, and jobs (jobId, title, location, postedAgo, benefits, easyApply, url). Pass only a companyId from get_company_info - slugs are rejected and an invalid id makes LinkedIn silently drop the filter and return total 0 (indistinguishable from no openings); postedAgo is null on a "Viewed" marker.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_company_jobs`
- Updated: 2026-09-03 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_company_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_company_jobs
```

## Input

- `companyId` (string | integer, required): Numeric inner LinkedIn company ID (e.g. 3008681). This is the companyId returned by linkedin.com/get_company_info — chain from it; slugs are NOT accepted here. Battle-tested caveat: an unknown/invalid id makes LinkedIn silently DROP the company filter and the script returns total 0 — indistinguishable from a company with no openings, so only pass ids that came from get_company_info.
- `page` (integer, optional): 1-based page, 25 jobs per page (start=(page-1)*25). Caller loops while (page-1)*25 < total. A page beyond the last one returns the no-results state (total 0), so don't probe blindly. Job lists move as postings open/close; cross-page fan-out can skip/dupe near edits.
- `geoId` (string | integer, optional): LinkedIn geo filter. Defaults to 92000000 = Worldwide ON PURPOSE: the UI's own default silently restricts to the viewer's country (battle-tested: 39 US results vs 48 worldwide for the same company).
- `keywords` (string, optional): Optional free-text filter within the company's jobs (same as the search box).

## Output

- `jobs` (array, required)
- `page` (integer, required)
- `total` (integer, required): Total open postings for this filter, read from the SSR blob ('N results' header). 0 with empty jobs[] = company has no matching openings (first-class outcome, not an error).

## FAQ

### What does "Get LinkedIn company jobs" do?

Get a LinkedIn company's open job postings by numeric companyId, worldwide by default, paginated (25/page). Returns total, page, and jobs (jobId, title, location, postedAgo, benefits, easyApply, url). Pass only a companyId from get_company_info - slugs are rejected and an invalid id makes LinkedIn silently drop the filter and return total 0 (indistinguishable from no openings); postedAgo is null on a "Viewed" marker.

### How do I automatically get LinkedIn company jobs on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_company_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_company_jobs

### Is there a linkedin.com API to get LinkedIn company jobs?

You do not need one. "Get LinkedIn company jobs" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: companyId. Optional: page, geoId, keywords.

### What does it return?

It returns jobs, page, total.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

Unknown: its author has not declared whether it changes anything on linkedin.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_company_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_company_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_company_jobs
