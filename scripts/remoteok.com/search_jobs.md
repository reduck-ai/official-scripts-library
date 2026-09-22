# Search RemoteOK jobs

Automatically search RemoteOK jobs on remoteok.com. Search RemoteOK's full live listings database — a fuzzy, ordered full-text match across every posting, the same as the site's own search box, not just the most recent ones. Omit query for the unfiltered recent feed. Paginates via offset, in pages of about 50. Salary is reconciled against RemoteOK's own published listing data, because the salary attached to a search result is frequently a generic 90000-150000 placeholder unrelated to the actual role.

- Site: remoteok.com
- Address: `reduck/remoteok.com/search_jobs`
- Updated: 2026-09-13 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/remoteok.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/remoteok.com/search_jobs
```

## Input

- `query` (string, optional): Full-text search against RemoteOK's own search index (same fuzzy, ordered-match behavior as the site's search box), run across its entire live listings database — not just the most recent postings. Omit for the unfiltered recent-postings feed.
- `offset` (integer, optional): Row offset for pagination; the site returns pages of up to 50 jobs. Loop increasing by 50 until a call returns fewer than 50 jobs. This is a live, moving feed — dedupe by `id` when merging pages fetched at different times.

## Output

- `jobs` (array, required)

## FAQ

### What does "Search RemoteOK jobs" do?

Search RemoteOK's full live listings database — a fuzzy, ordered full-text match across every posting, the same as the site's own search box, not just the most recent ones. Omit query for the unfiltered recent feed. Paginates via offset, in pages of about 50. Salary is reconciled against RemoteOK's own published listing data, because the salary attached to a search result is frequently a generic 90000-150000 placeholder unrelated to the actual role.

### How do I automatically search RemoteOK jobs on remoteok.com?

Ask an AI agent connected to Reduck to run reduck/remoteok.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/remoteok.com/search_jobs

### Is there a remoteok.com API to search RemoteOK jobs?

You do not need one. "Search RemoteOK jobs" drives the real remoteok.com pages in a browser, so it works whether or not remoteok.com offers an API for this.

### What information do I need to provide?

Optional: query, offset.

### What does it return?

It returns jobs.

### Do I need to be logged in to remoteok.com?

No. It only uses pages of remoteok.com that are reachable without signing in.

### Does it change anything on remoteok.com, or only read data?

Unknown: its author has not declared whether it changes anything on remoteok.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/remoteok.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/remoteok.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/remoteok.com/search_jobs
