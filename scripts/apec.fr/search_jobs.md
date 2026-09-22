# Search APEC jobs

Automatically search APEC jobs on apec.fr. Search APEC (French executive/manager job board) listings by keyword, optional free-text location, and page (20 offers/page). Returns total and jobs (jobId, title, company, url, location, salary, snippet, confidential, datePublication). Location is free text resolved to a commune/department/region code (same as picking the first suggestion in the UI) — an unrecognized location throws instead of silently searching nationwide. Only executive/manager-track roles are listed (APEC's own site scope, not a script-added restriction). Company and salary are null for offers the poster chose not to disclose (frequent for confidential searches).

- Site: apec.fr
- Address: `reduck/apec.fr/search_jobs`
- Updated: 2026-08-17 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/apec.fr/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/apec.fr/search_jobs
```

## Input

- `query` (string, required): Free-text job search query, same as APEC's own search box (e.g. "data engineer").
- `page` (integer, optional): 1-based page, 20 offers per page (APEC's own default page size).
- `location` (string, optional): Free-text location (e.g. "Paris", "Lyon"). Omit to search all of France. Resolved server-side to APEC's own location code; an unrecognized location throws rather than silently searching nationwide.

## Output

- `jobs` (array, required)
- `page` (integer, required)
- `total` (integer, required): Matching offer count reported by APEC's API (totalCount). 0 with empty jobs[] = no matching offers (first-class outcome, not an error).

## FAQ

### What does "Search APEC jobs" do?

Search APEC (French executive/manager job board) listings by keyword, optional free-text location, and page (20 offers/page). Returns total and jobs (jobId, title, company, url, location, salary, snippet, confidential, datePublication). Location is free text resolved to a commune/department/region code (same as picking the first suggestion in the UI) — an unrecognized location throws instead of silently searching nationwide. Only executive/manager-track roles are listed (APEC's own site scope, not a script-added restriction). Company and salary are null for offers the poster chose not to disclose (frequent for confidential searches).

### How do I automatically search APEC jobs on apec.fr?

Ask an AI agent connected to Reduck to run reduck/apec.fr/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/apec.fr/search_jobs

### Is there a apec.fr API to search APEC jobs?

You do not need one. "Search APEC jobs" drives the real apec.fr pages in a browser, so it works whether or not apec.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, location.

### What does it return?

It returns jobs, page, total.

### Do I need to be logged in to apec.fr?

No. It only uses pages of apec.fr that are reachable without signing in.

### Does it change anything on apec.fr, or only read data?

Unknown: its author has not declared whether it changes anything on apec.fr, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/apec.fr/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/apec.fr/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/apec.fr/search_jobs
