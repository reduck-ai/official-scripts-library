# Get Glassdoor salary estimates

Automatically get Glassdoor salary estimates on glassdoor.com. Get Glassdoor's base-pay distribution (10th, 25th, median, 75th and 90th percentile) for a job title in a chosen country, with no sign-in. A title Glassdoor has no figures for is refused. Glassdoor serves a country's figures only to a browser on a network in that country; otherwise the request is refused.

- Site: glassdoor.com
- Address: `reduck/glassdoor.com/get_salaries`
- Updated: 2026-11-03 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/glassdoor.com/get_salaries`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/glassdoor.com/get_salaries
```

## Input

- `job_title` (string, required): Job title slug words, e.g. "software engineer" (used to build the URL slug)
- `country` (string, optional): Country to get salary data for. Glassdoor serves each country from its own domain and the site itself force-redirects a visitor to their geo's domain regardless of URL params, so 'United States' can only be honored when the browser's own network is US-based — from any other geo it throws rather than silently returning that geo's figures instead. Omit to get whatever country Glassdoor's own geo-detection resolves the session to.

## Output

- `available` (boolean, required): Always true: a title with no salary data is refused.
- `job_title` (string, required)
- `median` (number | null, optional)
- `currency` (string | null, optional)
- `location` (string | null, optional)
- `percentile10` (number | null, optional)
- `percentile25` (number | null, optional)
- `percentile75` (number | null, optional)
- `percentile90` (number | null, optional)

## FAQ

### What does "Get Glassdoor salary estimates" do?

Get Glassdoor's base-pay distribution (10th, 25th, median, 75th and 90th percentile) for a job title in a chosen country, with no sign-in. A title Glassdoor has no figures for is refused. Glassdoor serves a country's figures only to a browser on a network in that country; otherwise the request is refused.

### How do I automatically get Glassdoor salary estimates on glassdoor.com?

Ask an AI agent connected to Reduck to run reduck/glassdoor.com/get_salaries, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/glassdoor.com/get_salaries

### Is there a glassdoor.com API to get Glassdoor salary estimates?

You do not need one. "Get Glassdoor salary estimates" drives the real glassdoor.com pages in a browser, so it works whether or not glassdoor.com offers an API for this.

### What information do I need to provide?

Required: job_title. Optional: country.

### What does it return?

It returns median, currency, location, available, job_title, percentile10, percentile25, percentile75, percentile90.

### Do I need to be logged in to glassdoor.com?

No. It only uses pages of glassdoor.com that are reachable without signing in.

### Does it change anything on glassdoor.com, or only read data?

It only reads. It looks things up on glassdoor.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/glassdoor.com/get_salaries, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/glassdoor.com/get_salaries

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/glassdoor.com/get_salaries
