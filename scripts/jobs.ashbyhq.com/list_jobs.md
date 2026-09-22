# List job board postings

Automatically list job board postings on jobs.ashbyhq.com. List every open position on an Ashby-hosted job board (jobs.ashbyhq.com/&lt;board&gt;).

- Site: jobs.ashbyhq.com
- Address: `reduck/jobs.ashbyhq.com/list_jobs`
- Updated: 2026-08-02 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/jobs.ashbyhq.com/list_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/jobs.ashbyhq.com/list_jobs
```

## Input

- `board` (string, required): Board slug in the URL jobs.ashbyhq.com/<board>, e.g. "lassie" or "ramp". Case-sensitive.

## Output

- `jobs` (array, required): Every open position the board lists, alphabetically by title (the board's own data order, not the department grouping the page renders). Ashby boards are not paginated, so this is the full set; empty when the board has no open positions.
- `organization` (string, required): Company name the board belongs to.

## FAQ

### What does "List job board postings" do?

List every open position on an Ashby-hosted job board (jobs.ashbyhq.com/&lt;board&gt;).

### How do I automatically list job board postings on jobs.ashbyhq.com?

Ask an AI agent connected to Reduck to run reduck/jobs.ashbyhq.com/list_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jobs.ashbyhq.com/list_jobs

### Is there a jobs.ashbyhq.com API to list job board postings?

You do not need one. "List job board postings" drives the real jobs.ashbyhq.com pages in a browser, so it works whether or not jobs.ashbyhq.com offers an API for this.

### What information do I need to provide?

Required: board.

### What does it return?

It returns jobs, organization.

### Do I need to be logged in to jobs.ashbyhq.com?

No. It only uses pages of jobs.ashbyhq.com that are reachable without signing in.

### Does it change anything on jobs.ashbyhq.com, or only read data?

Unknown: its author has not declared whether it changes anything on jobs.ashbyhq.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/jobs.ashbyhq.com/list_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jobs.ashbyhq.com/list_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/jobs.ashbyhq.com/list_jobs
