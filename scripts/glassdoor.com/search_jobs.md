# Search Glassdoor jobs

Automatically search Glassdoor jobs on glassdoor.com. Search Glassdoor job listings by keyword and optional free-text location (city). Returns total and jobs (jobId, title, url, company, rating, location, salary, snippet, postedAgo) for the first results page (~30 listings — Glassdoor's pagination is a JS "load more" action, not a URL param, and was observed to break the page outright on click, so only page 1 is supported here). Location is resolved via Glassdoor's own place-autocomplete, preferring the first city-level match, because the top overall suggestion can be a broader state or region record that Glassdoor then silently fails to filter by; an unrecognized or non-filtering location throws. Glassdoor serves the UI (and some listing labels like the skills line) in whatever language/locale it geo-resolves the session to, independent of the job's own country — text fields may not be in English or in the language of the job itself. Distinct from the existing search_companies/get_company scripts, which cover company profiles and reviews, not job postings.

- Site: glassdoor.com
- Address: `reduck/glassdoor.com/search_jobs`
- Updated: 2026-08-26 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/glassdoor.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/glassdoor.com/search_jobs
```

## Input

- `query` (string, required): Free-text job search query, same as Glassdoor's own search box (e.g. "data engineer").
- `location` (string, optional): Free-text city (e.g. "Paris", "Los Angeles"). Omit to search without a location filter. Resolved via Glassdoor's own autocomplete; an unrecognized or non-filtering location throws rather than silently returning unrelated/broader results.

## Output

- `jobs` (array, required)
- `total` (integer | null, required): Matching job count reported by Glassdoor's results headline. null if the headline couldn't be parsed.

## FAQ

### What does "Search Glassdoor jobs" do?

Search Glassdoor job listings by keyword and optional free-text location (city). Returns total and jobs (jobId, title, url, company, rating, location, salary, snippet, postedAgo) for the first results page (~30 listings — Glassdoor's pagination is a JS "load more" action, not a URL param, and was observed to break the page outright on click, so only page 1 is supported here). Location is resolved via Glassdoor's own place-autocomplete, preferring the first city-level match, because the top overall suggestion can be a broader state or region record that Glassdoor then silently fails to filter by; an unrecognized or non-filtering location throws. Glassdoor serves the UI (and some listing labels like the skills line) in whatever language/locale it geo-resolves the session to, independent of the job's own country — text fields may not be in English or in the language of the job itself. Distinct from the existing search_companies/get_company scripts, which cover company profiles and reviews, not job postings.

### How do I automatically search Glassdoor jobs on glassdoor.com?

Ask an AI agent connected to Reduck to run reduck/glassdoor.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/glassdoor.com/search_jobs

### Is there a glassdoor.com API to search Glassdoor jobs?

You do not need one. "Search Glassdoor jobs" drives the real glassdoor.com pages in a browser, so it works whether or not glassdoor.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: location.

### What does it return?

It returns jobs, total.

### Do I need to be logged in to glassdoor.com?

No. It only uses pages of glassdoor.com that are reachable without signing in.

### Does it change anything on glassdoor.com, or only read data?

It only reads. It looks things up on glassdoor.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/glassdoor.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/glassdoor.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/glassdoor.com/search_jobs
