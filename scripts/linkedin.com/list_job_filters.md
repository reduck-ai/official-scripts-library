# List LinkedIn job search filters

Automatically list LinkedIn job search filters on linkedin.com. List the filters LinkedIn's jobs search offers for a search, with the options each one shows and LinkedIn's ids for them: places inside the area, companies, industries, job functions, titles, benefits, commitments, salary buckets, experience levels, job types, workplace types, distance, date posted and the yes/no filters. Each filter names the linkedin.com/search_jobs arg that takes its ids. The options are the short list LinkedIn shows in its filter panel for this search, not every possible value, and they change with the keywords and place.

- Site: linkedin.com
- Address: `reduck/linkedin.com/list_job_filters`
- Updated: 2026-10-28 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/list_job_filters`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/list_job_filters
```

## Input

- `geoId` (string, optional): LinkedIn geo id of the place, from linkedin.com/suggest_locations. Takes precedence over location. Omit both for worldwide.
- `keywords` (string, optional): Free-text job search query. The options shown depend on it. Omit for all jobs.
- `location` (string, optional): Free-text place. LinkedIn picks the place itself.
- `companyIds` (array, optional): Company ids to select, so the company filter shows their names and whether LinkedIn knows them.

## Output

- `filters` (array, required)

## FAQ

### What does "List LinkedIn job search filters" do?

List the filters LinkedIn's jobs search offers for a search, with the options each one shows and LinkedIn's ids for them: places inside the area, companies, industries, job functions, titles, benefits, commitments, salary buckets, experience levels, job types, workplace types, distance, date posted and the yes/no filters. Each filter names the linkedin.com/search_jobs arg that takes its ids. The options are the short list LinkedIn shows in its filter panel for this search, not every possible value, and they change with the keywords and place.

### How do I automatically list LinkedIn job search filters on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/list_job_filters, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/list_job_filters

### Is there a linkedin.com API to list LinkedIn job search filters?

You do not need one. "List LinkedIn job search filters" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: geoId, keywords, location, companyIds.

### What does it return?

It returns filters.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/list_job_filters, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/list_job_filters

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/list_job_filters
