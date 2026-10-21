# Search Welcome to the Jungle candidates across all jobs

Automatically search Welcome to the Jungle candidates across all jobs on welcomekit.co. Search all candidates of a Welcome to the Jungle ATS organization across every job at once (the dashboard's global candidate search), with an optional text query. Returns one page of 20 candidates, newest first, with each candidate's profile fields and the direct link to their card, plus the total count and nextPage to pass for the next page (null on the last page). A query with no match returns an empty list. Fails with a signed-out error when the browser is not signed in.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/search_all_candidates`
- Updated: 2026-10-20 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/search_all_candidates`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/search_all_candidates
```

## Input

- `org` (string, required): Organization reference as it appears in your dashboard URL https://www.welcomekit.co/dashboard/o/<org>/ (6-char code).
- `page` (integer, optional): Result page, starting at 0 (20 candidates per page, newest first). Pass nextPage from the previous call.
- `query` (string, optional): Free-text search, same as typing in the dashboard's candidate search box (matches name, email, job, stage, address, comments, reviews...).

## Output

- `org` (string, required)
- `page` (integer, required)
- `query` (string, required)
- `nextPage` (integer | null, required): Page to pass for the next results; null on the last page.
- `candidates` (array, required)
- `totalPages` (integer, required)
- `totalMatching` (integer, required): Total candidates matching the query that this account can see.

## FAQ

### What does "Search Welcome to the Jungle candidates across all jobs" do?

Search all candidates of a Welcome to the Jungle ATS organization across every job at once (the dashboard's global candidate search), with an optional text query. Returns one page of 20 candidates, newest first, with each candidate's profile fields and the direct link to their card, plus the total count and nextPage to pass for the next page (null on the last page). A query with no match returns an empty list. Fails with a signed-out error when the browser is not signed in.

### How do I automatically search Welcome to the Jungle candidates across all jobs on welcomekit.co?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/search_all_candidates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/search_all_candidates

### Is there a welcomekit.co API to search Welcome to the Jungle candidates across all jobs?

You do not need one. "Search Welcome to the Jungle candidates across all jobs" drives the real welcomekit.co pages in a browser, so it works whether or not welcomekit.co offers an API for this.

### What information do I need to provide?

Required: org. Optional: page, query.

### What does it return?

It returns org, page, query, nextPage, candidates, totalPages, totalMatching.

### Do I need to be logged in to welcomekit.co?

Yes. It acts as you on welcomekit.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the welcomekit.co cookies saved by the Reduck extension.

### Does it change anything on welcomekit.co, or only read data?

It only reads. It looks things up on welcomekit.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/search_all_candidates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/search_all_candidates

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/search_all_candidates
