# Search Wizbii jobs

Automatically search Wizbii jobs on wizbii.com. Searches job listings on jobs.wizbii.com by filtering by business domain (slug required, e.g. developpement-informatique, marketing, ventes — full list at wizbii.com/directory/lp/domaine) and optionally by city (slug, e.g. paris, lyon — list at wizbii.com/directory/lp/ville). No free-text keyword search: the site only exposes this category×city filter. Returns the site's own richer listing data for each result. An invalid domain or city throws explicitly rather than returning an empty page. 1-based pagination, matching the site's own URL.

- Site: wizbii.com
- Address: `reduck/wizbii.com/search_jobs`
- Updated: 2026-08-14 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/wizbii.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/wizbii.com/search_jobs
```

## Input

- `domain` (string, required): Wizbii business domain slug, e.g. "developpement-informatique", "marketing", "ventes", "comptabilite-controle-de-gestion", "rh-formation". Full list at wizbii.com/directory/lp/domaine.
- `city` (string, optional): Optional city slug, e.g. "paris", "lyon". Must match an existing city on the site (see wizbii.com/directory/lp/ville).
- `page` (integer, optional): Page number, 1-based, as in the site's URL (?page=N). Defaults to 1.

## Output

- `jobs` (array, required)
- `page` (integer, required): Current page, 0-based (as returned by Algolia)
- `nbHits` (integer, required): Total number of listings matching the filter
- `nbPages` (integer, required): Total number of pages

## FAQ

### What does "Search Wizbii jobs" do?

Searches job listings on jobs.wizbii.com by filtering by business domain (slug required, e.g. developpement-informatique, marketing, ventes — full list at wizbii.com/directory/lp/domaine) and optionally by city (slug, e.g. paris, lyon — list at wizbii.com/directory/lp/ville). No free-text keyword search: the site only exposes this category×city filter. Returns the site's own richer listing data for each result. An invalid domain or city throws explicitly rather than returning an empty page. 1-based pagination, matching the site's own URL.

### How do I automatically search Wizbii jobs on wizbii.com?

Ask an AI agent connected to Reduck to run reduck/wizbii.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wizbii.com/search_jobs

### Is there a wizbii.com API to search Wizbii jobs?

You do not need one. "Search Wizbii jobs" drives the real wizbii.com pages in a browser, so it works whether or not wizbii.com offers an API for this.

### What information do I need to provide?

Required: domain. Optional: city, page.

### What does it return?

It returns jobs, page, nbHits, nbPages.

### Do I need to be logged in to wizbii.com?

No. It only uses pages of wizbii.com that are reachable without signing in.

### Does it change anything on wizbii.com, or only read data?

It only reads. It looks things up on wizbii.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/wizbii.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wizbii.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/wizbii.com/search_jobs
