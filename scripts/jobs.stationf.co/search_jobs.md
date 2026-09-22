# Search Station F jobs

Automatically search Station F jobs on jobs.stationf.co. Search job listings on Station F's public careers board (jobs.stationf.co, an embeddable careers widget aggregating openings across Station F resident startups) by free-text keyword and optional filters: department/profession (site's own category label, e.g. "Tech", "Business", "Sales", "Operations", "Comm / Marketing"), city (e.g. "Paris"), and contractType (site's own English label, e.g. "Full-Time", "Internship", "Apprenticeship", "Fixed-Term"). Filter values must match the site's own labels exactly — an unrecognized value throws rather than silently searching unfiltered. Pagination is 1-based via page; requesting a page beyond what's available throws rather than silently returning page 1. Returns total, page, totalPages, and jobs (id, reference, slug, title, url, company {name, slug, employees, logoUrl}, department, profession, contractType + contractTypeLabel, remote, salary, office, offices, publishedAt, promoted). A query/filter combination with no matches returns an empty jobs list, not an error.

- Site: jobs.stationf.co
- Address: `reduck/jobs.stationf.co/search_jobs`
- Updated: 2026-08-28 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/jobs.stationf.co/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/jobs.stationf.co/search_jobs
```

## Input

- `city` (string, optional): Exact city facet label as shown on the site, e.g. "Paris"
- `page` (integer, optional): 1-based page number. Must be within the visible pagination window for the current query/filters (throws otherwise).
- `query` (string, optional): Free-text keyword, e.g. "developer", "product manager"
- `department` (string, optional): Exact department/profession facet label as shown on the site, e.g. "Tech", "Business", "Sales", "Operations"
- `contractType` (string, optional): Exact contract-type facet label as shown on the site (English), e.g. "Full-Time", "Internship", "Apprenticeship", "Fixed-Term"

## Output

- `jobs` (array, optional)
- `page` (integer, optional)
- `total` (integer, optional)
- `totalPages` (integer, optional)

## FAQ

### What does "Search Station F jobs" do?

Search job listings on Station F's public careers board (jobs.stationf.co, an embeddable careers widget aggregating openings across Station F resident startups) by free-text keyword and optional filters: department/profession (site's own category label, e.g. "Tech", "Business", "Sales", "Operations", "Comm / Marketing"), city (e.g. "Paris"), and contractType (site's own English label, e.g. "Full-Time", "Internship", "Apprenticeship", "Fixed-Term"). Filter values must match the site's own labels exactly — an unrecognized value throws rather than silently searching unfiltered. Pagination is 1-based via page; requesting a page beyond what's available throws rather than silently returning page 1. Returns total, page, totalPages, and jobs (id, reference, slug, title, url, company {name, slug, employees, logoUrl}, department, profession, contractType + contractTypeLabel, remote, salary, office, offices, publishedAt, promoted). A query/filter combination with no matches returns an empty jobs list, not an error.

### How do I automatically search Station F jobs on jobs.stationf.co?

Ask an AI agent connected to Reduck to run reduck/jobs.stationf.co/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jobs.stationf.co/search_jobs

### Is there a jobs.stationf.co API to search Station F jobs?

You do not need one. "Search Station F jobs" drives the real jobs.stationf.co pages in a browser, so it works whether or not jobs.stationf.co offers an API for this.

### What information do I need to provide?

Optional: city, page, query, department, contractType.

### What does it return?

It returns jobs, page, total, totalPages.

### Do I need to be logged in to jobs.stationf.co?

No. It only uses pages of jobs.stationf.co that are reachable without signing in.

### Does it change anything on jobs.stationf.co, or only read data?

It only reads. It looks things up on jobs.stationf.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/jobs.stationf.co/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jobs.stationf.co/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/jobs.stationf.co/search_jobs
