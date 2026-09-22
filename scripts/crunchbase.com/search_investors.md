# Crunchbase: Search Investors

Automatically search Investors on crunchbase.com. Filtered investor search on Crunchbase, by investor type, HQ location, and number of investments/exits. Returns up to 15 matching investors (Crunchbase's free-tier search limit).

- Site: crunchbase.com
- Address: `reduck/crunchbase.com/search_investors`
- Updated: 2026-07-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crunchbase.com/search_investors`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/search_investors
```

## Input

- `limit` (number, optional): Max investors to return, 1-15. Crunchbase's free tier hard-caps search results at 15 regardless of the true match count. Default 15.
- `locations` (array, optional): Location names (city, region, country, or continent), e.g. "France", "Europe". Matched investors must be headquartered in ANY of the given locations.
- `minNumExits` (number, optional): Minimum number of exits (acquisitions/IPOs) among this investor's portfolio.
- `investorTypes` (array, optional): Crunchbase investor-type slugs to filter on. Matched investors must have ANY of the given types.
- `minNumInvestments` (number, optional): Minimum number of funding rounds this investor has participated in.

## Output

- `investors` (array, required)
- `totalMatchCount` (number, required): Total number of investors matching the filters on Crunchbase, before the 15-result free-tier cap is applied.

## FAQ

### What does "Crunchbase: Search Investors" do?

Filtered investor search on Crunchbase, by investor type, HQ location, and number of investments/exits. Returns up to 15 matching investors (Crunchbase's free-tier search limit).

### How do I automatically search Investors on crunchbase.com?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/search_investors, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/search_investors

### Is there a crunchbase.com API to search Investors?

You do not need one. "Crunchbase: Search Investors" drives the real crunchbase.com pages in a browser, so it works whether or not crunchbase.com offers an API for this.

### What information do I need to provide?

Optional: limit, locations, minNumExits, investorTypes, minNumInvestments.

### What does it return?

It returns investors, totalMatchCount.

### Do I need to be logged in to crunchbase.com?

Yes. It acts as you on crunchbase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the crunchbase.com cookies saved by the Reduck extension.

### Does it change anything on crunchbase.com, or only read data?

Unknown: its author has not declared whether it changes anything on crunchbase.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/search_investors, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/search_investors

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/crunchbase.com/search_investors
