# Search Behance jobs

Automatically search Behance jobs on behance.net. Search Behance's job board (freelance briefs and full-time/contract listings) by keyword, returning title, company, location, remote status, job type, salary and url.

- Site: behance.net
- Address: `reduck/behance.net/search_jobs`
- Updated: 2026-08-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/behance.net/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/behance.net/search_jobs
```

## Input

- `query` (string, optional): Search keywords, e.g. "illustrator". Omit to list all jobs.
- `jobType` (string, optional): Filter by job type. Omit for all types.

## Output

- `results` (array, required)

## FAQ

### What does "Search Behance jobs" do?

Search Behance's job board (freelance briefs and full-time/contract listings) by keyword, returning title, company, location, remote status, job type, salary and url.

### How do I automatically search Behance jobs on behance.net?

Ask an AI agent connected to Reduck to run reduck/behance.net/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/behance.net/search_jobs

### Is there a behance.net API to search Behance jobs?

You do not need one. "Search Behance jobs" drives the real behance.net pages in a browser, so it works whether or not behance.net offers an API for this.

### What information do I need to provide?

Optional: query, jobType.

### What does it return?

It returns results.

### Do I need to be logged in to behance.net?

No. It only uses pages of behance.net that are reachable without signing in.

### Does it change anything on behance.net, or only read data?

It only reads. It looks things up on behance.net and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/behance.net/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/behance.net/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/behance.net/search_jobs
