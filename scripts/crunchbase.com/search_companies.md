# Crunchbase: Search Companies

Automatically search Companies on crunchbase.com. Filtered company search on Crunchbase, by industry, HQ location, funding stage, funding amount, and founded date range. Returns up to 15 matching companies (Crunchbase's free-tier search limit).

- Site: crunchbase.com
- Address: `reduck/crunchbase.com/search_companies`
- Updated: 2026-07-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crunchbase.com/search_companies`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/search_companies
```

## Input

- `limit` (number, optional): Max companies to return, 1-15. Crunchbase's free tier hard-caps search results at 15 regardless of the true match count. Default 15.
- `locations` (array, optional): Location names (city, region, country, or continent), e.g. "France", "Paris", "Europe". Matched companies must be headquartered in ANY of the given locations.
- `industries` (array, optional): Industry/category names as typed on Crunchbase, e.g. "Fintech", "SaaS". Each is resolved to Crunchbase's category via autocomplete; matched companies must have ANY of the given industries.
- `foundedAfter` (string, optional): Only companies founded on/after this date, YYYY-MM-DD.
- `foundedBefore` (string, optional): Only companies founded on/before this date, YYYY-MM-DD.
- `lastFundingTypes` (array, optional): Funding stage slugs to filter the company's most recent round, e.g. "seed", "series_a", "series_b", "debt_financing", "private_equity". Passed through as-is to Crunchbase (must match its internal slug).
- `maxFundingTotalUsd` (number, optional): Maximum total funding raised, in USD.
- `minFundingTotalUsd` (number, optional): Minimum total funding raised, in USD.

## Output

- `companies` (array, required)
- `totalMatchCount` (number, required): Total number of companies matching the filters on Crunchbase, before the 15-result free-tier cap is applied.

## FAQ

### What does "Crunchbase: Search Companies" do?

Filtered company search on Crunchbase, by industry, HQ location, funding stage, funding amount, and founded date range. Returns up to 15 matching companies (Crunchbase's free-tier search limit).

### How do I automatically search Companies on crunchbase.com?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/search_companies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/search_companies

### Is there a crunchbase.com API to search Companies?

You do not need one. "Crunchbase: Search Companies" drives the real crunchbase.com pages in a browser, so it works whether or not crunchbase.com offers an API for this.

### What information do I need to provide?

Optional: limit, locations, industries, foundedAfter, foundedBefore, lastFundingTypes, maxFundingTotalUsd, minFundingTotalUsd.

### What does it return?

It returns companies, totalMatchCount.

### Do I need to be logged in to crunchbase.com?

Yes. It acts as you on crunchbase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the crunchbase.com cookies saved by the Reduck extension.

### Does it change anything on crunchbase.com, or only read data?

Unknown: its author has not declared whether it changes anything on crunchbase.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/search_companies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/search_companies

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/crunchbase.com/search_companies
