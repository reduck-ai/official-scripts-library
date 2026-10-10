# Search the Meta (Facebook) Ad Library

Automatically search the Meta (Facebook) Ad Library on facebook.com. Search Meta's public Ad Library for ads running on Facebook, Instagram, Messenger and Threads, by keyword or by advertiser page, in one country or all. Returns each ad's library id and link, advertiser page, active status, start and end dates, platforms, ad text, headline, landing link, call to action, image and video links, and how many versions it has. No account needed.

- Site: facebook.com
- Address: `reduck/facebook.com/ads_library_search`
- Updated: 2026-10-09 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/ads_library_search`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/ads_library_search
```

## Input

- `limit` (integer, optional): Maximum ads to return (default 25, about one page). Above that, further pages are loaded; Facebook may rate-limit those from datacenter browsers.
- `query` (string, optional): Keyword or advertiser name to search for. Required unless pageId is given.
- `adType` (string, optional): Default all.
- `pageId` (string, optional): Numeric Facebook page id to list all ads of one advertiser (the pageId returned by this script).
- `country` (string, optional): 2-letter ISO country code where the ads ran (e.g. FR, US), or ALL. Default ALL.
- `mediaType` (string, optional): Default all.
- `exactPhrase` (boolean, optional): Match the query as an exact phrase instead of any of its words.
- `activeStatus` (string, optional): Default active.

## Output

- `ads` (array, required)
- `count` (integer, required)
- `query` (string | null, optional)
- `pageId` (string | null, optional)
- `country` (string, optional)
- `hasMore` (boolean, optional)
- `totalApprox` (integer | null, optional): Meta's own approximate result count.
- `activeStatus` (string, optional)

## FAQ

### What does "Search the Meta (Facebook) Ad Library" do?

Search Meta's public Ad Library for ads running on Facebook, Instagram, Messenger and Threads, by keyword or by advertiser page, in one country or all. Returns each ad's library id and link, advertiser page, active status, start and end dates, platforms, ad text, headline, landing link, call to action, image and video links, and how many versions it has. No account needed.

### How do I automatically search the Meta (Facebook) Ad Library on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/ads_library_search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/ads_library_search

### Is there a facebook.com API to search the Meta (Facebook) Ad Library?

You do not need one. "Search the Meta (Facebook) Ad Library" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Optional: limit, query, adType, pageId, country, mediaType, exactPhrase, activeStatus.

### What does it return?

It returns ads, count, query, pageId, country, hasMore, totalApprox, activeStatus.

### Do I need to be logged in to facebook.com?

No. It only uses pages of facebook.com that are reachable without signing in.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/ads_library_search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/ads_library_search

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/ads_library_search
