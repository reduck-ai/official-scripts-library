# Workable: Get company jobs

Automatically get company jobs on workable.com. Lists a company's open job postings on its Workable job board (apply.workable.com/<slug>): id, shortcode, title, department, location, remote, workplace, type, published date and link. Pass nextToken from the previous call as token to get the next page; nextToken is null on the last page. A board with no openings returns total 0 and an empty list; an unknown slug fails with an error.

- Site: workable.com
- Address: `reduck/workable.com/get_company_jobs`
- Updated: 2026-11-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/workable.com/get_company_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/workable.com/get_company_jobs
```

## Input

- `slug` (string, required): Workable board slug, e.g. "treatwell" for apply.workable.com/treatwell
- `token` (string, optional): Opaque pagination cursor returned as nextToken from a previous call. Omit for the first page.

## Output

- `jobs` (array, required)
- `total` (integer, required)
- `nextToken` (string | null, required)

## FAQ

### What does "Workable: Get company jobs" do?

Lists a company's open job postings on its Workable job board (apply.workable.com/<slug>): id, shortcode, title, department, location, remote, workplace, type, published date and link. Pass nextToken from the previous call as token to get the next page; nextToken is null on the last page. A board with no openings returns total 0 and an empty list; an unknown slug fails with an error.

### How do I automatically get company jobs on workable.com?

Ask an AI agent connected to Reduck to run reduck/workable.com/get_company_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/workable.com/get_company_jobs

### Is there a workable.com API to get company jobs?

You do not need one. "Workable: Get company jobs" drives the real workable.com pages in a browser, so it works whether or not workable.com offers an API for this.

### What information do I need to provide?

Required: slug. Optional: token.

### What does it return?

It returns jobs, total, nextToken.

### Do I need to be logged in to workable.com?

No. It only uses pages of workable.com that are reachable without signing in.

### Does it change anything on workable.com, or only read data?

Unknown: its author has not declared whether it changes anything on workable.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/workable.com/get_company_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/workable.com/get_company_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/workable.com/get_company_jobs
