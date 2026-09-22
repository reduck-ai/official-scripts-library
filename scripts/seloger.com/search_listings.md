# Search SeLoger listings

Automatically search SeLoger listings on seloger.com. Search SeLoger listings by location and deal type. Returns page, count, total, and listings, each with id, url, title, propertyType, price, pricePerSqm, surface, rooms, bedrooms, floor, location, postalCode, and agency. location must be a 'city-dept' slug (e.g. paris-75, lyon-69); results are paginated, so fetch successive pages for the full set. For areas with few local listings, SeLoger widens the search radius and appends nearby recommendations in the same listing format, so count/listings.length can exceed total (the exact-match count for the searched location).

- Site: seloger.com
- Address: `reduck/seloger.com/search_listings`
- Updated: 2026-08-14 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/seloger.com/search_listings`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/seloger.com/search_listings
```

## Input

- `location` (string, required): Human slug 'city-dept', e.g. paris-75, lyon-69, marseille-13
- `deal` (string, optional)
- `page` (integer, optional)

## Output

- `url` (string, required)
- `page` (number, required)
- `count` (number, required)
- `total` (number | null, required)
- `listings` (array, required)

## FAQ

### What does "Search SeLoger listings" do?

Search SeLoger listings by location and deal type. Returns page, count, total, and listings, each with id, url, title, propertyType, price, pricePerSqm, surface, rooms, bedrooms, floor, location, postalCode, and agency. location must be a 'city-dept' slug (e.g. paris-75, lyon-69); results are paginated, so fetch successive pages for the full set. For areas with few local listings, SeLoger widens the search radius and appends nearby recommendations in the same listing format, so count/listings.length can exceed total (the exact-match count for the searched location).

### How do I automatically search SeLoger listings on seloger.com?

Ask an AI agent connected to Reduck to run reduck/seloger.com/search_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/seloger.com/search_listings

### Is there a seloger.com API to search SeLoger listings?

You do not need one. "Search SeLoger listings" drives the real seloger.com pages in a browser, so it works whether or not seloger.com offers an API for this.

### What information do I need to provide?

Required: location. Optional: deal, page.

### What does it return?

It returns url, page, count, total, listings.

### Do I need to be logged in to seloger.com?

No. It only uses pages of seloger.com that are reachable without signing in.

### Does it change anything on seloger.com, or only read data?

It only reads. It looks things up on seloger.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/seloger.com/search_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/seloger.com/search_listings

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/seloger.com/search_listings
