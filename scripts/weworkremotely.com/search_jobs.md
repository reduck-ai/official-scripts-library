# Search WeWorkRemotely jobs

Automatically search WeWorkRemotely jobs on weworkremotely.com. Search We Work Remotely two ways: `query` hits the site's own "Search everything" full-text search (leaner fields: no absolute date, just relative postedAgo, plus salaryRange/companyHeadquarters); `category` reads the RSS feed for one category or the combined feed (richer fields: region/country/state/skills/absolute pubDate, no free-text search). They're separate site affordances, not merged — query takes priority if both are given.

- Site: weworkremotely.com
- Address: `reduck/weworkremotely.com/search_jobs`
- Updated: 2026-09-13 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/weworkremotely.com/search_jobs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/weworkremotely.com/search_jobs
```

## Input

- `query` (string, optional): Full-text search against WWR's own search index (title/company), same as the site's 'Search everything' box, run across its entire live listings database. Takes priority over category if both are given — they hit different site affordances and aren't combined server-side.
- `category` (string, optional): WWR category slug from the site's own nav, e.g. 'remote-front-end-programming-jobs', 'remote-back-end-programming-jobs', 'remote-full-stack-programming-jobs', 'remote-design-jobs', 'remote-devops-sysadmin-jobs', 'remote-management-and-finance-jobs', 'remote-product-jobs', 'remote-customer-support-jobs', 'remote-sales-and-marketing-jobs', 'all-other-remote-jobs'. Ignored if query is given. Omit both for the combined all-categories feed.

## Output

- `jobs` (array, required)

## FAQ

### What does "Search WeWorkRemotely jobs" do?

Search We Work Remotely two ways: `query` hits the site's own "Search everything" full-text search (leaner fields: no absolute date, just relative postedAgo, plus salaryRange/companyHeadquarters); `category` reads the RSS feed for one category or the combined feed (richer fields: region/country/state/skills/absolute pubDate, no free-text search). They're separate site affordances, not merged — query takes priority if both are given.

### How do I automatically search WeWorkRemotely jobs on weworkremotely.com?

Ask an AI agent connected to Reduck to run reduck/weworkremotely.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/weworkremotely.com/search_jobs

### Is there a weworkremotely.com API to search WeWorkRemotely jobs?

You do not need one. "Search WeWorkRemotely jobs" drives the real weworkremotely.com pages in a browser, so it works whether or not weworkremotely.com offers an API for this.

### What information do I need to provide?

Optional: query, category.

### What does it return?

It returns jobs.

### Do I need to be logged in to weworkremotely.com?

No. It only uses pages of weworkremotely.com that are reachable without signing in.

### Does it change anything on weworkremotely.com, or only read data?

Unknown: its author has not declared whether it changes anything on weworkremotely.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/weworkremotely.com/search_jobs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/weworkremotely.com/search_jobs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/weworkremotely.com/search_jobs
