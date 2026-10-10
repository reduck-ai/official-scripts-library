# Search France Travail jobs

Automatically search France Travail jobs on francetravail.fr. Search France Travail (formerly Pôle Emploi) public job listings by keyword, optional free-text location (city or department) or location code, and page (20 offers/page). Returns jobs (jobId, title, company, location, description, contract, postedAgo, url) and, on page 1 only, the total match count. An ambiguous or unrecognized location is refused rather than silently searching nationwide.

- Site: francetravail.fr
- Address: `reduck/francetravail.fr/search_jobs`
- Updated: 2026-10-09 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/francetravail.fr/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/francetravail.fr/search_jobs
```

## Input

- `query` (string, required): Free-text job search query, same as France Travail's own search box (e.g. "data engineer").
- `page` (integer, optional): 1-based page, 20 offers per page.
- `lieux` (string, optional): France Travail location code, if you already know it: a department code with a D suffix (e.g. "75D") or a commune code (e.g. "69123" = Lyon). Skips the location lookup. Takes precedence over location.
- `location` (string, optional): City or department name (e.g. "Lyon"). Omit to search all of France. Only used when it matches one commune or department exactly (or France Travail returns a single place); when several match (e.g. "Paris" is both), the run refuses and lists their lieux codes so you can pass the right one. The place used is returned as resolvedLocation.

## Output

- `jobs` (array, required)
- `page` (integer, required)
- `total` (integer | null, optional): Matching offer count reported by France Travail's results header. Only populated on page 1 (the page>1 fragment endpoint doesn't repeat it) — null on later pages. 0 with empty jobs[] on page 1 = no matching offers (first-class outcome, not an error).
- `resolvedLocation` (object | null, optional): The place the search was filtered on (null when no location was given). label/type are null when lieux was passed directly.

## FAQ

### What does "Search France Travail jobs" do?

Search France Travail (formerly Pôle Emploi) public job listings by keyword, optional free-text location (city or department) or location code, and page (20 offers/page). Returns jobs (jobId, title, company, location, description, contract, postedAgo, url) and, on page 1 only, the total match count. An ambiguous or unrecognized location is refused rather than silently searching nationwide.

### How do I automatically search France Travail jobs on francetravail.fr?

Ask an AI agent connected to Reduck to run reduck/francetravail.fr/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/francetravail.fr/search_jobs

### Is there a francetravail.fr API to search France Travail jobs?

You do not need one. "Search France Travail jobs" drives the real francetravail.fr pages in a browser, so it works whether or not francetravail.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, lieux, location.

### What does it return?

It returns jobs, page, total, resolvedLocation.

### Do I need to be logged in to francetravail.fr?

No. It only uses pages of francetravail.fr that are reachable without signing in.

### Does it change anything on francetravail.fr, or only read data?

It only reads. It looks things up on francetravail.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/francetravail.fr/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/francetravail.fr/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/francetravail.fr/search_jobs
