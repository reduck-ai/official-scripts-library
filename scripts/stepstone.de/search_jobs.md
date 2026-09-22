# Search StepStone (Germany) jobs

Automatically search StepStone (Germany) jobs on stepstone.de. Search StepStone.de's German job listings by free-text keyword and optional free-text location. Returns total and jobs (id, title, url, company, companyUrl, location, salary, workFromHome, datePosted, snippet, quickApply). Pagination is 1-based (arg page), 25 results per page. Both an unmatched keyword and an unrecognized location legitimately return total:0, jobs:[] — StepStone's own location matching is strict (no silent nationwide fallback), so this is a real empty result, not a coerced one.

- Site: stepstone.de
- Address: `reduck/stepstone.de/search_jobs`
- Updated: 2026-08-14 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/stepstone.de/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/stepstone.de/search_jobs
```

## Input

- `page` (integer, optional): 1-based page number, 25 results per page. Defaults to 1.
- `query` (string, optional): Free-text keyword, e.g. 'Entwickler'. Omit to browse all jobs.
- `location` (string, optional): Free-text city name, e.g. 'Berlin'. Omit for nationwide search.

## Output

- `jobs` (array, required)
- `total` (integer, required)

## FAQ

### What does "Search StepStone (Germany) jobs" do?

Search StepStone.de's German job listings by free-text keyword and optional free-text location. Returns total and jobs (id, title, url, company, companyUrl, location, salary, workFromHome, datePosted, snippet, quickApply). Pagination is 1-based (arg page), 25 results per page. Both an unmatched keyword and an unrecognized location legitimately return total:0, jobs:[] — StepStone's own location matching is strict (no silent nationwide fallback), so this is a real empty result, not a coerced one.

### How do I automatically search StepStone (Germany) jobs on stepstone.de?

Ask an AI agent connected to Reduck to run reduck/stepstone.de/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/stepstone.de/search_jobs

### Is there a stepstone.de API to search StepStone (Germany) jobs?

You do not need one. "Search StepStone (Germany) jobs" drives the real stepstone.de pages in a browser, so it works whether or not stepstone.de offers an API for this.

### What information do I need to provide?

Optional: page, query, location.

### What does it return?

It returns jobs, total.

### Do I need to be logged in to stepstone.de?

No. It only uses pages of stepstone.de that are reachable without signing in.

### Does it change anything on stepstone.de, or only read data?

It only reads. It looks things up on stepstone.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/stepstone.de/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/stepstone.de/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/stepstone.de/search_jobs
