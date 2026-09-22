# Search restaurants near a coordinate

Automatically search restaurants near a coordinate on thefork.com. Search TheFork restaurants near a lat/lng, one page (site paginates 25/page). Returns pagination (totalCount/totalPage/hasNext) and per-restaurant: name, address, coords, distanceM from the input point, theforkRating (/10) plus reviews, avgPriceEur, priceRangeLevel, cuisine, promoPct (max %% discount in deals) and raw deals, url. Results come back in the site's default quality order, not by distance, so filter by distanceM caller-side and loop `page` to totalPage.

- Site: thefork.com
- Address: `reduck/thefork.com/search_nearby`
- Updated: 2026-08-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/thefork.com/search_nearby`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/thefork.com/search_nearby
```

## Input

- `latitude` (number, required): Latitude of the search center (e.g. 48.8682613).
- `longitude` (number, required): Longitude of the search center (e.g. 2.3443572).
- `page` (integer, optional): 1-based result page; site returns 25/page. Loop 1..totalPage to get all.

## Output

- `page` (integer, optional)
- `count` (integer, optional)
- `hasNext` (boolean, optional)
- `totalPage` (integer, optional)
- `totalCount` (integer, optional)
- `restaurants` (array, optional)

## FAQ

### What does "Search restaurants near a coordinate" do?

Search TheFork restaurants near a lat/lng, one page (site paginates 25/page). Returns pagination (totalCount/totalPage/hasNext) and per-restaurant: name, address, coords, distanceM from the input point, theforkRating (/10) plus reviews, avgPriceEur, priceRangeLevel, cuisine, promoPct (max %% discount in deals) and raw deals, url. Results come back in the site's default quality order, not by distance, so filter by distanceM caller-side and loop `page` to totalPage.

### How do I automatically search restaurants near a coordinate on thefork.com?

Ask an AI agent connected to Reduck to run reduck/thefork.com/search_nearby, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/thefork.com/search_nearby

### Is there a thefork.com API to search restaurants near a coordinate?

You do not need one. "Search restaurants near a coordinate" drives the real thefork.com pages in a browser, so it works whether or not thefork.com offers an API for this.

### What information do I need to provide?

Required: latitude, longitude. Optional: page.

### What does it return?

It returns page, count, hasNext, totalPage, totalCount, restaurants.

### Do I need to be logged in to thefork.com?

No. It only uses pages of thefork.com that are reachable without signing in.

### Does it change anything on thefork.com, or only read data?

Unknown: its author has not declared whether it changes anything on thefork.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/thefork.com/search_nearby, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/thefork.com/search_nearby

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/thefork.com/search_nearby
