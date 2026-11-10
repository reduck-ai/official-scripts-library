# Crunchbase: Search Companies

Automatically search Companies on crunchbase.com. Search Crunchbase companies by industry, headquarters location, last funding type, total funding and founding date. Returns up to 15 companies, most prominent first, and the total match count.

- Site: crunchbase.com
- Address: `reduck/crunchbase.com/search_companies`
- Updated: 2026-11-09 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crunchbase.com/search_companies`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/search_companies
```

## Input

- `limit` (integer, optional): How many companies to return, 1 to 15 (Crunchbase's free plan shows at most 15).
- `locations` (array, optional): Headquarters location names (city, region, country or continent), e.g. "France", "Paris". Companies in any of them match.
- `industries` (array, optional): Industry names as Crunchbase shows them, e.g. "Fintech", "SaaS". Companies in any of them match.
- `foundedAfter` (string, optional): Only companies founded on or after this date, YYYY-MM-DD.
- `foundedBefore` (string, optional): Only companies founded on or before this date, YYYY-MM-DD.
- `lastFundingTypes` (array, optional): Type of the company's last funding round, as Crunchbase names it, e.g. "seed", "series_a", "series_b", "debt_financing", "private_equity".
- `maxFundingTotalUsd` (number, optional): Maximum total funding raised, in USD.
- `minFundingTotalUsd` (number, optional): Minimum total funding raised, in USD.

## Output

- `companies` (array, required)
- `totalMatchCount` (number, required): How many companies match on Crunchbase, before the 15-result limit.

## FAQ

### What does "Crunchbase: Search Companies" do?

Search Crunchbase companies by industry, headquarters location, last funding type, total funding and founding date. Returns up to 15 companies, most prominent first, and the total match count.

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

It only reads. It looks things up on crunchbase.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/search_companies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/search_companies

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/crunchbase.com/search_companies
