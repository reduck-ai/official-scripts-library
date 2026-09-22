# Search Welcome to the Jungle candidates across all jobs

Automatically search Welcome to the Jungle candidates across all jobs on welcomekit.co. Search all candidates of a Welcome to the Jungle ATS organization across every job at once (the dashboard's global candidate search), with an optional text query, stopping once applications go past a given date. Returns each candidate's profile fields and the direct link to their card.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/search_all_candidates`
- Updated: 2026-09-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/search_all_candidates`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/search_all_candidates
```

## Input

- `org` (string, required): Organization reference as it appears in your dashboard URL https://www.welcomekit.co/dashboard/o/<org>/ (6-char code).
- `sinceDate` (string, required): ISO date (e.g. 2026-08-01) or datetime. The search stops paginating once it reaches applications created before this date; candidates older than it are not returned.
- `query` (string, optional): Free-text search, same as typing in the dashboard's candidate search box (matches name, email, job, stage, address, comments, reviews...).
- `maxPages` (integer, optional): Safety cap on how many result pages (20 candidates each) to fetch before stopping, in case sinceDate is never reached.

## Output

- `org` (string, required)
- `query` (string, required)
- `sinceDate` (string, required)
- `candidates` (array, required)
- `pagesFetched` (integer, required)
- `totalMatching` (integer, required): Total candidates matching the query across the whole organization, per the search index (before the date cutoff is applied).
- `reachedSinceDate` (boolean, required): True if pagination stopped because it reached applications older than sinceDate; false if it stopped because there were no more results or maxPages was hit first.

## FAQ

### What does "Search Welcome to the Jungle candidates across all jobs" do?

Search all candidates of a Welcome to the Jungle ATS organization across every job at once (the dashboard's global candidate search), with an optional text query, stopping once applications go past a given date. Returns each candidate's profile fields and the direct link to their card.

### How do I automatically search Welcome to the Jungle candidates across all jobs on welcomekit.co?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/search_all_candidates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/search_all_candidates

### Is there a welcomekit.co API to search Welcome to the Jungle candidates across all jobs?

You do not need one. "Search Welcome to the Jungle candidates across all jobs" drives the real welcomekit.co pages in a browser, so it works whether or not welcomekit.co offers an API for this.

### What information do I need to provide?

Required: org, sinceDate. Optional: query, maxPages.

### What does it return?

It returns org, query, sinceDate, candidates, pagesFetched, totalMatching, reachedSinceDate.

### Do I need to be logged in to welcomekit.co?

Yes. It acts as you on welcomekit.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the welcomekit.co cookies saved by the Reduck extension.

### Does it change anything on welcomekit.co, or only read data?

It only reads. It looks things up on welcomekit.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/search_all_candidates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/search_all_candidates

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/search_all_candidates
