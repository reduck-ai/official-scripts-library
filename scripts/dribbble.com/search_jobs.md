# Search Dribbble jobs

Automatically search Dribbble jobs on dribbble.com. Search Dribbble's job board by keyword, location and job type, returning title, company, location, posted date and url.

- Site: dribbble.com
- Address: `reduck/dribbble.com/search_jobs`
- Updated: 2026-08-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dribbble.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dribbble.com/search_jobs
```

## Input

- `jobType` (string, optional): Filter by job type. Omit for all types.
- `keyword` (string, optional): Search by company, skill or tag, e.g. "illustrator". Omit to list all jobs.
- `location` (string, optional): Location filter, e.g. "New York". Omit for any location.

## Output

- `results` (array, required)

## FAQ

### What does "Search Dribbble jobs" do?

Search Dribbble's job board by keyword, location and job type, returning title, company, location, posted date and url.

### How do I automatically search Dribbble jobs on dribbble.com?

Ask an AI agent connected to Reduck to run reduck/dribbble.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dribbble.com/search_jobs

### Is there a dribbble.com API to search Dribbble jobs?

You do not need one. "Search Dribbble jobs" drives the real dribbble.com pages in a browser, so it works whether or not dribbble.com offers an API for this.

### What information do I need to provide?

Optional: jobType, keyword, location.

### What does it return?

It returns results.

### Do I need to be logged in to dribbble.com?

No. It only uses pages of dribbble.com that are reachable without signing in.

### Does it change anything on dribbble.com, or only read data?

Unknown: its author has not declared whether it changes anything on dribbble.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dribbble.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dribbble.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dribbble.com/search_jobs
