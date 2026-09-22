# Crunchbase: Get Recent Funding Rounds

Automatically get Recent Funding Rounds on crunchbase.com. Recent funding rounds on Crunchbase, filtered by the funded company's industry/location, round type, and amount/date range. Returns up to 15 matching rounds (Crunchbase's free-tier search limit).

- Site: crunchbase.com
- Address: `reduck/crunchbase.com/get_recent_funding_rounds`
- Updated: 2026-07-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crunchbase.com/get_recent_funding_rounds`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_recent_funding_rounds
```

## Input

- `limit` (number, optional): Max rounds to return, 1-15. Crunchbase's free tier hard-caps search results at 15 regardless of the true match count. Default 15.
- `locations` (array, optional): Location names (city, region, country, or continent) of the funded company's HQ, e.g. "France", "Europe".
- `industries` (array, optional): Industry/category names of the funded company, e.g. "Fintech", "SaaS". Matched rounds must belong to a company with ANY of the given industries.
- `announcedAfter` (string, optional): Only rounds announced on/after this date, YYYY-MM-DD.
- `announcedBefore` (string, optional): Only rounds announced on/before this date, YYYY-MM-DD.
- `investmentTypes` (array, optional): Round-type slugs, e.g. "seed", "series_a", "series_b", "debt_financing".
- `minMoneyRaisedUsd` (number, optional): Minimum amount raised in this round, in USD.

## Output

- `fundingRounds` (array, required)
- `totalMatchCount` (number, required): Total number of rounds matching the filters on Crunchbase, before the 15-result free-tier cap is applied.

## FAQ

### What does "Crunchbase: Get Recent Funding Rounds" do?

Recent funding rounds on Crunchbase, filtered by the funded company's industry/location, round type, and amount/date range. Returns up to 15 matching rounds (Crunchbase's free-tier search limit).

### How do I automatically get Recent Funding Rounds on crunchbase.com?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/get_recent_funding_rounds, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_recent_funding_rounds

### Is there a crunchbase.com API to get Recent Funding Rounds?

You do not need one. "Crunchbase: Get Recent Funding Rounds" drives the real crunchbase.com pages in a browser, so it works whether or not crunchbase.com offers an API for this.

### What information do I need to provide?

Optional: limit, locations, industries, announcedAfter, announcedBefore, investmentTypes, minMoneyRaisedUsd.

### What does it return?

It returns fundingRounds, totalMatchCount.

### Do I need to be logged in to crunchbase.com?

Yes. It acts as you on crunchbase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the crunchbase.com cookies saved by the Reduck extension.

### Does it change anything on crunchbase.com, or only read data?

Unknown: its author has not declared whether it changes anything on crunchbase.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/get_recent_funding_rounds, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_recent_funding_rounds

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/crunchbase.com/get_recent_funding_rounds
