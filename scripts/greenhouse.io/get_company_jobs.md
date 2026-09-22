# Greenhouse: get company jobs

Automatically get company jobs on greenhouse.io. Fetch a company's live job postings from Greenhouse's public board API by board slug (boards.greenhouse.io/<slug>). Anonymous, no auth. Returns id, title, location, department(s), url, updatedAt, firstPublished. Throws (job board not found) if the slug isn't a Greenhouse customer.

- Site: greenhouse.io
- Address: `reduck/greenhouse.io/get_company_jobs`
- Updated: 2026-08-17 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/greenhouse.io/get_company_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/greenhouse.io/get_company_jobs
```

## Input

- `slug` (string, required): Greenhouse board slug, e.g. "airbnb" for boards.greenhouse.io/airbnb

## Output

- `jobs` (array, required)
- `slug` (string, required)
- `total` (integer, required)

## FAQ

### What does "Greenhouse: get company jobs" do?

Fetch a company's live job postings from Greenhouse's public board API by board slug (boards.greenhouse.io/<slug>). Anonymous, no auth. Returns id, title, location, department(s), url, updatedAt, firstPublished. Throws (job board not found) if the slug isn't a Greenhouse customer.

### How do I automatically get company jobs on greenhouse.io?

Ask an AI agent connected to Reduck to run reduck/greenhouse.io/get_company_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/greenhouse.io/get_company_jobs

### Is there a greenhouse.io API to get company jobs?

You do not need one. "Greenhouse: get company jobs" drives the real greenhouse.io pages in a browser, so it works whether or not greenhouse.io offers an API for this.

### What information do I need to provide?

Required: slug.

### What does it return?

It returns jobs, slug, total.

### Do I need to be logged in to greenhouse.io?

No. It only uses pages of greenhouse.io that are reachable without signing in.

### Does it change anything on greenhouse.io, or only read data?

Unknown: its author has not declared whether it changes anything on greenhouse.io, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/greenhouse.io/get_company_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/greenhouse.io/get_company_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/greenhouse.io/get_company_jobs
