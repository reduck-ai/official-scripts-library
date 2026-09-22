# Get Similarweb website traffic overview

Automatically get Similarweb website traffic overview on similarweb.com. Fetch a website's traffic overview from Similarweb: global/country/category rank, bounce rate, pages per visit, avg visit duration, and company profile fields. No login required.

- Site: similarweb.com
- Address: `reduck/similarweb.com/get_traffic`
- Updated: 2026-09-21 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/similarweb.com/get_traffic`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/similarweb.com/get_traffic
```

## Input

- `domain` (string, required): Website domain, e.g. "notion.so" or "spotify.com"

## Output

- `domain` (string, required)
- `available` (boolean, required): False when Similarweb has no report for this domain — an expected outcome for small or unknown sites, not an error.
- `hq` (string | null, optional)
- `company` (string | null, optional)
- `country` (string | null, optional)
- `category` (string | null, optional)
- `industry` (string | null, optional)
- `employees` (string | null, optional)
- `bounceRate` (string | null, optional): Null when the page renders a placeholder instead of a figure.
- `globalRank` (integer | null, optional)
- `countryRank` (integer | null, optional)
- `yearFounded` (string | null, optional)
- `categoryRank` (integer | null, optional)
- `annualRevenue` (string | null, optional)
- `pagesPerVisit` (string | null, optional): Null when the page renders a placeholder instead of a figure.
- `avgVisitDuration` (string | null, optional): Null when the page renders a placeholder instead of a figure.

## FAQ

### What does "Get Similarweb website traffic overview" do?

Fetch a website's traffic overview from Similarweb: global/country/category rank, bounce rate, pages per visit, avg visit duration, and company profile fields. No login required.

### How do I automatically get Similarweb website traffic overview on similarweb.com?

Ask an AI agent connected to Reduck to run reduck/similarweb.com/get_traffic, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/similarweb.com/get_traffic

### Is there a similarweb.com API to get Similarweb website traffic overview?

You do not need one. "Get Similarweb website traffic overview" drives the real similarweb.com pages in a browser, so it works whether or not similarweb.com offers an API for this.

### What information do I need to provide?

Required: domain.

### What does it return?

It returns hq, domain, company, country, category, industry, available, employees, bounceRate, globalRank, countryRank, yearFounded, categoryRank, annualRevenue, pagesPerVisit, avgVisitDuration.

### Do I need to be logged in to similarweb.com?

No. It only uses pages of similarweb.com that are reachable without signing in.

### Does it change anything on similarweb.com, or only read data?

It only reads. It looks things up on similarweb.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/similarweb.com/get_traffic, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/similarweb.com/get_traffic

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/similarweb.com/get_traffic
