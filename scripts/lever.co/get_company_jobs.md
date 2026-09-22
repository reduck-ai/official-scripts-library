# Lever: get company jobs

Automatically get company jobs on lever.co. Fetch a company's live job postings from Lever's public postings API by board slug (jobs.lever.co/<slug>). Anonymous, no auth. Returns id, title, team, location(s), commitment, url, createdAt. Empty array if the company posts nothing right now; throws only on a genuine API error (not on "no jobs").

- Site: lever.co
- Address: `reduck/lever.co/get_company_jobs`
- Updated: 2026-08-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lever.co/get_company_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lever.co/get_company_jobs
```

## Input

- `slug` (string, required): Lever board slug, e.g. "palantir" for jobs.lever.co/palantir

## Output

- `jobs` (array, required)
- `slug` (string, required)
- `total` (integer, required)

## FAQ

### What does "Lever: get company jobs" do?

Fetch a company's live job postings from Lever's public postings API by board slug (jobs.lever.co/<slug>). Anonymous, no auth. Returns id, title, team, location(s), commitment, url, createdAt. Empty array if the company posts nothing right now; throws only on a genuine API error (not on "no jobs").

### How do I automatically get company jobs on lever.co?

Ask an AI agent connected to Reduck to run reduck/lever.co/get_company_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lever.co/get_company_jobs

### Is there a lever.co API to get company jobs?

You do not need one. "Lever: get company jobs" drives the real lever.co pages in a browser, so it works whether or not lever.co offers an API for this.

### What information do I need to provide?

Required: slug.

### What does it return?

It returns jobs, slug, total.

### Do I need to be logged in to lever.co?

No. It only uses pages of lever.co that are reachable without signing in.

### Does it change anything on lever.co, or only read data?

It only reads. It looks things up on lever.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lever.co/get_company_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lever.co/get_company_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/lever.co/get_company_jobs
