# Search ZipRecruiter.com jobs

Automatically search ZipRecruiter.com jobs on ziprecruiter.de. Search ZipRecruiter job listings by keyword and optional free-text location, 20 per page. ZipRecruiter answers from the country site of the browser's network location (returned as edition). Some cards have no description, and some links are sponsored redirects.

- Site: ziprecruiter.de
- Address: `reduck/ziprecruiter.de/search_jobs`
- Updated: 2026-11-23 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ziprecruiter.de/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ziprecruiter.de/search_jobs
```

## Input

- `query` (string, required): Keyword to search (job title, skill, company).
- `page` (integer, optional): 1-based page number, 20 results per page.
- `location` (string, optional): Free-text location (city or region), as typed in the site's search box. Omit to search without a location.

## Output

- `jobs` (array, required)
- `page` (integer, required)
- `query` (string, required)
- `edition` (string, required): The ZipRecruiter country site that answered (e.g. https://www.ziprecruiter.de); it depends on the network location of the browser.
- `location` (string | null, required): The location searched, or null when none was given.
- `totalResults` (integer | null, required): Total result count the site reports, or null when it shows none.

## FAQ

### What does "Search ZipRecruiter.com jobs" do?

Search ZipRecruiter job listings by keyword and optional free-text location, 20 per page. ZipRecruiter answers from the country site of the browser's network location (returned as edition). Some cards have no description, and some links are sponsored redirects.

### How do I automatically search ZipRecruiter.com jobs on ziprecruiter.de?

Ask an AI agent connected to Reduck to run reduck/ziprecruiter.de/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ziprecruiter.de/search_jobs

### Is there a ziprecruiter.de API to search ZipRecruiter.com jobs?

You do not need one. "Search ZipRecruiter.com jobs" drives the real ziprecruiter.de pages in a browser, so it works whether or not ziprecruiter.de offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, location.

### What does it return?

It returns jobs, page, query, edition, location, totalResults.

### Do I need to be logged in to ziprecruiter.de?

No. It only uses pages of ziprecruiter.de that are reachable without signing in.

### Does it change anything on ziprecruiter.de, or only read data?

It only reads. It looks things up on ziprecruiter.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ziprecruiter.de/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ziprecruiter.de/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ziprecruiter.de/search_jobs
