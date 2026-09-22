# Search France Travail jobs

Automatically search France Travail jobs on francetravail.fr. Search France Travail (formerly Pôle Emploi) public job listings by keyword, optional free-text location (city or department), and page (20 offers/page). Returns total (page 1 only) and jobs (jobId, title, company, location, description, contract, postedAgo, url). Location free text is resolved via France Travail's own public geo API to a commune or department code (same as picking the first suggestion in the UI); an unrecognized location throws instead of silently searching nationwide. Page 1 is read directly from the results page; later pages are fetched via the site's own "load more" mechanism. total is only returned for page 1 — later pages don't repeat it.

- Site: francetravail.fr
- Address: `reduck/francetravail.fr/search_jobs`
- Updated: 2026-09-10 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/francetravail.fr/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/francetravail.fr/search_jobs
```

## Input

- `query` (string, required): Free-text job search query, same as France Travail's own search box (e.g. "data engineer").
- `page` (integer, optional): 1-based page, 20 offers per page.
- `location` (string, optional): Free-text location: a city or department name (e.g. "Lyon", "Paris"). Omit to search all of France. Resolved server-side to France Travail's own commune/department code; an unrecognized location throws rather than silently searching nationwide. Only commune- and department-level matches are supported (not region or country).

## Output

- `jobs` (array, required)
- `page` (integer, required)
- `total` (integer | null, optional): Matching offer count reported by France Travail's results header. Only populated on page 1 (the page>1 fragment endpoint doesn't repeat it) — null on later pages. 0 with empty jobs[] on page 1 = no matching offers (first-class outcome, not an error).

## FAQ

### What does "Search France Travail jobs" do?

Search France Travail (formerly Pôle Emploi) public job listings by keyword, optional free-text location (city or department), and page (20 offers/page). Returns total (page 1 only) and jobs (jobId, title, company, location, description, contract, postedAgo, url). Location free text is resolved via France Travail's own public geo API to a commune or department code (same as picking the first suggestion in the UI); an unrecognized location throws instead of silently searching nationwide. Page 1 is read directly from the results page; later pages are fetched via the site's own "load more" mechanism. total is only returned for page 1 — later pages don't repeat it.

### How do I automatically search France Travail jobs on francetravail.fr?

Ask an AI agent connected to Reduck to run reduck/francetravail.fr/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/francetravail.fr/search_jobs

### Is there a francetravail.fr API to search France Travail jobs?

You do not need one. "Search France Travail jobs" drives the real francetravail.fr pages in a browser, so it works whether or not francetravail.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, location.

### What does it return?

It returns jobs, page, total.

### Do I need to be logged in to francetravail.fr?

No. It only uses pages of francetravail.fr that are reachable without signing in.

### Does it change anything on francetravail.fr, or only read data?

It only reads. It looks things up on francetravail.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/francetravail.fr/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/francetravail.fr/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/francetravail.fr/search_jobs
