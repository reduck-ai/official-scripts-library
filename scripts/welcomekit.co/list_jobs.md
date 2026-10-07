# List ATS jobs

Automatically list ATS jobs on welcomekit.co. List jobs in the Welcome to the Jungle ATS by status. Returns jobs with id, name, reference, status, pipeline stages, and candidate counts (new/inProcess/refused). reference is the join key for list_job_candidates.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/list_jobs`
- Updated: 2026-10-06 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/list_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/list_jobs
```

## Input

- `org` (string, required): Organization reference as it appears in your dashboard URL https://www.welcomekit.co/dashboard/o/<org>/ (6-char code).
- `limit` (integer, optional)
- `query` (string, optional): Free-text filter on job name (server-side). Omit for all.
- `offset` (integer, optional): Pagination offset. Order is lastActivityAt DESC.
- `status` (string, optional)

## Output

- `org` (string, required)
- `jobs` (array, required)
- `status` (string, required)

## FAQ

### What does "List ATS jobs" do?

List jobs in the Welcome to the Jungle ATS by status. Returns jobs with id, name, reference, status, pipeline stages, and candidate counts (new/inProcess/refused). reference is the join key for list_job_candidates.

### How do I automatically list ATS jobs on welcomekit.co?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/list_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/list_jobs

### Is there a welcomekit.co API to list ATS jobs?

You do not need one. "List ATS jobs" drives the real welcomekit.co pages in a browser, so it works whether or not welcomekit.co offers an API for this.

### What information do I need to provide?

Required: org. Optional: limit, query, offset, status.

### What does it return?

It returns org, jobs, status.

### Do I need to be logged in to welcomekit.co?

Yes. It acts as you on welcomekit.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the welcomekit.co cookies saved by the Reduck extension.

### Does it change anything on welcomekit.co, or only read data?

It only reads. It looks things up on welcomekit.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/list_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/list_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/list_jobs
