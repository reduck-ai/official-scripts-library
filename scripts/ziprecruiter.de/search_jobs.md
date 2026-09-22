# Search ZipRecruiter.com jobs

Automatically search ZipRecruiter.com jobs on ziprecruiter.de. Search ZipRecruiter job listings by keyword + optional location, paginated 20/page. Adapts to whichever country edition the caller's own session lands on (starts at ziprecruiter.com; ZipRecruiter itself redirects based on network location — a German-resolving session ends up on .de, others may stay on .com) — the served edition is returned as `edition`, so behavior legitimately varies by caller. Location is resolved via that edition's own geocoder when available; if an edition doesn't support it, the location is passed through as free text instead of failing (see `locationNote`). Verified end-to-end on Germany- and France-resolving sessions; other editions are assumed compatible (same underlying platform) but unverified. On the France edition, list cards don't render a description snippet at all, so `description` is always null there — this is the site's own per-edition markup, not missing data. Some listing URLs are third-party ad-click redirects rather than direct job pages — that's the site's own sponsored-listing behavior.

- Site: ziprecruiter.de
- Address: `reduck/ziprecruiter.de/search_jobs`
- Updated: 2026-08-14 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ziprecruiter.de/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ziprecruiter.de/search_jobs
```

## Input

- `query` (string, required): Keyword to search (job title, skill, company). Required.
- `page` (integer, optional): 1-based page number, 20 results per page.
- `location` (string, optional): Free-text location (city/region). Resolved via ZipRecruiter's own geocoder when available on the caller's edition; otherwise passed through as free text. Omit to use the site's default location (geo-IP based).

## Output

- `jobs` (array, required)
- `page` (integer, required)
- `query` (string, required)
- `edition` (string, required): The ZipRecruiter country-edition origin the caller's own session actually landed on (e.g. https://www.ziprecruiter.de or https://www.ziprecruiter.com) — depends on the caller's network location, not fixed by this script.
- `location` (string | null, required): Resolved location label, or null if none was given/resolved.
- `totalResults` (integer | null, required): Total result count reported by the site for this query, or null if zero results.
- `locationNote` (string | null, optional): Set when this edition's geocoder endpoint wasn't available and the location was passed through as free text instead of a resolved place. Null otherwise.

## FAQ

### What does "Search ZipRecruiter.com jobs" do?

Search ZipRecruiter job listings by keyword + optional location, paginated 20/page. Adapts to whichever country edition the caller's own session lands on (starts at ziprecruiter.com; ZipRecruiter itself redirects based on network location — a German-resolving session ends up on .de, others may stay on .com) — the served edition is returned as `edition`, so behavior legitimately varies by caller. Location is resolved via that edition's own geocoder when available; if an edition doesn't support it, the location is passed through as free text instead of failing (see `locationNote`). Verified end-to-end on Germany- and France-resolving sessions; other editions are assumed compatible (same underlying platform) but unverified. On the France edition, list cards don't render a description snippet at all, so `description` is always null there — this is the site's own per-edition markup, not missing data. Some listing URLs are third-party ad-click redirects rather than direct job pages — that's the site's own sponsored-listing behavior.

### How do I automatically search ZipRecruiter.com jobs on ziprecruiter.de?

Ask an AI agent connected to Reduck to run reduck/ziprecruiter.de/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ziprecruiter.de/search_jobs

### Is there a ziprecruiter.de API to search ZipRecruiter.com jobs?

You do not need one. "Search ZipRecruiter.com jobs" drives the real ziprecruiter.de pages in a browser, so it works whether or not ziprecruiter.de offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, location.

### What does it return?

It returns jobs, page, query, edition, location, locationNote, totalResults.

### Do I need to be logged in to ziprecruiter.de?

No. It only uses pages of ziprecruiter.de that are reachable without signing in.

### Does it change anything on ziprecruiter.de, or only read data?

Unknown: its author has not declared whether it changes anything on ziprecruiter.de, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ziprecruiter.de/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ziprecruiter.de/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ziprecruiter.de/search_jobs
