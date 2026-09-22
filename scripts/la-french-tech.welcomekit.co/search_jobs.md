# Search La French Tech jobs

Automatically search La French Tech jobs on la-french-tech.welcomekit.co. Search job listings on La French Tech's public careers board (la-french-tech.welcomekit.co, an embeddable careers widget aggregating openings across French Tech ecosystem startups) by free-text keyword and optional filters: department (site's own category, e.g. "Tech", "Sales", "Business" — French labels), city (e.g. "Paris", "Lyon"), and contractType (site's own French label, e.g. "CDI", "Stage", "Alternance", "CDD / Temporaire"). Filter values must match the site's own labels exactly — an unrecognized value throws rather than silently searching unfiltered. Pagination is 1-based via page; requesting a page beyond what's available throws rather than silently returning page 1. Returns total, page, totalPages, and jobs (id, reference, slug, title, url, company {name, slug, employees, logoUrl}, department, profession, contractType + contractTypeLabel, remote, salary, office, offices, publishedAt, promoted). A query/filter combination with no matches returns an empty jobs list, not an error.

- Site: la-french-tech.welcomekit.co
- Address: `reduck/la-french-tech.welcomekit.co/search_jobs`
- Updated: 2026-08-28 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/la-french-tech.welcomekit.co/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/la-french-tech.welcomekit.co/search_jobs
```

## Input

- `city` (string, optional): Exact city facet label as shown on the site, e.g. "Paris", "Lyon", "Barcelona"
- `page` (integer, optional): 1-based page number. Must be within the visible pagination window for the current query/filters (throws otherwise).
- `query` (string, optional): Free-text keyword, e.g. "developpeur", "product manager"
- `department` (string, optional): Exact department facet label as shown on the site, e.g. "Tech", "Sales", "Business", "Tech & Product"
- `contractType` (string, optional): Exact contract-type facet label as shown on the site (French), e.g. "CDI", "Stage", "Alternance", "CDD / Temporaire"

## Output

- `jobs` (array, optional)
- `page` (integer, optional)
- `total` (integer, optional)
- `totalPages` (integer, optional)

## FAQ

### What does "Search La French Tech jobs" do?

Search job listings on La French Tech's public careers board (la-french-tech.welcomekit.co, an embeddable careers widget aggregating openings across French Tech ecosystem startups) by free-text keyword and optional filters: department (site's own category, e.g. "Tech", "Sales", "Business" — French labels), city (e.g. "Paris", "Lyon"), and contractType (site's own French label, e.g. "CDI", "Stage", "Alternance", "CDD / Temporaire"). Filter values must match the site's own labels exactly — an unrecognized value throws rather than silently searching unfiltered. Pagination is 1-based via page; requesting a page beyond what's available throws rather than silently returning page 1. Returns total, page, totalPages, and jobs (id, reference, slug, title, url, company {name, slug, employees, logoUrl}, department, profession, contractType + contractTypeLabel, remote, salary, office, offices, publishedAt, promoted). A query/filter combination with no matches returns an empty jobs list, not an error.

### How do I automatically search La French Tech jobs on la-french-tech.welcomekit.co?

Ask an AI agent connected to Reduck to run reduck/la-french-tech.welcomekit.co/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/la-french-tech.welcomekit.co/search_jobs

### Is there a la-french-tech.welcomekit.co API to search La French Tech jobs?

You do not need one. "Search La French Tech jobs" drives the real la-french-tech.welcomekit.co pages in a browser, so it works whether or not la-french-tech.welcomekit.co offers an API for this.

### What information do I need to provide?

Optional: city, page, query, department, contractType.

### What does it return?

It returns jobs, page, total, totalPages.

### Do I need to be logged in to la-french-tech.welcomekit.co?

No. It only uses pages of la-french-tech.welcomekit.co that are reachable without signing in.

### Does it change anything on la-french-tech.welcomekit.co, or only read data?

It only reads. It looks things up on la-french-tech.welcomekit.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/la-french-tech.welcomekit.co/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/la-french-tech.welcomekit.co/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/la-french-tech.welcomekit.co/search_jobs
