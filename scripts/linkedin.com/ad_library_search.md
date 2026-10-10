# Search the LinkedIn Ad Library

Automatically search the LinkedIn Ad Library on linkedin.com. Search LinkedIn's public Ad Library by advertiser, payer or keyword, in chosen countries and date range. Returns each ad's id and detail link, ad format, the advertiser (company page or the person whose post is promoted, with their headline and the company promoting it), the ad text preview, headline and image links, plus LinkedIn's total match count. Returns about 24 ads per call by default. No LinkedIn account is used.

- Site: linkedin.com
- Address: `reduck/linkedin.com/ad_library_search`
- Updated: 2026-10-09 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/ad_library_search`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/ad_library_search
```

## Input

- `limit` (integer, optional): Maximum ads to return (default 24, about one page).
- `payer` (string, optional): Name of the entity that paid for the ads.
- `keyword` (string, optional): Word or phrase that appears in the ads.
- `countries` (array, optional): 2-letter ISO country codes where the ads were shown (e.g. ["FR","DE"]), or ["ALL"]. Default ALL.
- `advertiser` (string, optional): Company or advertiser name to search for (e.g. hubspot).
- `dateOption` (string, optional): Date range of the ads. Omit for LinkedIn's default (all available).

## Output

- `ads` (array, required)
- `count` (integer, required)
- `payer` (string | null, optional)
- `hasMore` (boolean, optional)
- `keyword` (string | null, optional)
- `countries` (array, optional)
- `advertiser` (string | null, optional)
- `totalApprox` (integer | null, optional)

## FAQ

### What does "Search the LinkedIn Ad Library" do?

Search LinkedIn's public Ad Library by advertiser, payer or keyword, in chosen countries and date range. Returns each ad's id and detail link, ad format, the advertiser (company page or the person whose post is promoted, with their headline and the company promoting it), the ad text preview, headline and image links, plus LinkedIn's total match count. Returns about 24 ads per call by default. No LinkedIn account is used.

### How do I automatically search the LinkedIn Ad Library on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/ad_library_search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/ad_library_search

### Is there a linkedin.com API to search the LinkedIn Ad Library?

You do not need one. "Search the LinkedIn Ad Library" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: limit, payer, keyword, countries, advertiser, dateOption.

### What does it return?

It returns ads, count, payer, hasMore, keyword, countries, advertiser, totalApprox.

### Do I need to be logged in to linkedin.com?

No. It only uses pages of linkedin.com that are reachable without signing in.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/ad_library_search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/ad_library_search

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/ad_library_search
