# Search Zillow listings

Automatically search Zillow listings on zillow.com. Search Zillow listings by location. Returns an array of cards with zpid, detailUrl, address, price, priceText, beds, baths, area, lat, lng, broker, imgSrc, statusText, and nearby. When too few listings match inside the region's boundary, Zillow relaxes the search to the surrounding area and shows those instead; those cards come back with nearby:true, so a narrow filter in a small neighbourhood can return results that are all nearby rather than in the region asked for. Pagination caps at 20 pages (about 820 listings) regardless of total matches, and relevance sort can drift between sessions, so use a deterministic sort like newest for parallel paging.

- Site: zillow.com
- Address: `reduck/zillow.com/search`
- Updated: 2026-09-02 (v15)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/zillow.com/search`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/zillow.com/search
```

## Input

- `location` (string, required): A human-readable location: city+state ("Austin, TX"), a ZIP code ("90210"), or a neighborhood. The path form resolves it to a Zillow region server-side.
- `page` (integer, optional): 1-based result page (41 listings each). Default 1. Zillow caps pagination at 20 pages (~820 listings) regardless of total matches.
- `sort` (string, optional): Sort order. Default "globalrelevanceex" (Homes for You) matches the site. When paging across independent browsers at the same time, pass a deterministic sort (e.g. "days" = newest) so pages partition identically — the default relevance order can drift between sessions.
- `status` (string, optional): Which Zillow listing category to search — the site's own For sale / For rent / Sold toggle, passed as its URL path segment. Default "for_sale". For-rent and recently-sold results include multi-unit building cards, which have no single price/beds/baths/area — those fields are null and the per-unit numbers are in `units` instead.
- `furnished` (boolean, optional): Restrict to Zillow's own "Furnished" rental filter. Only meaningful when status is for_rent — ignored for sale/sold listings. Default false = no restriction (all listings, furnished or not).

## FAQ

### What does "Search Zillow listings" do?

Search Zillow listings by location. Returns an array of cards with zpid, detailUrl, address, price, priceText, beds, baths, area, lat, lng, broker, imgSrc, statusText, and nearby. When too few listings match inside the region's boundary, Zillow relaxes the search to the surrounding area and shows those instead; those cards come back with nearby:true, so a narrow filter in a small neighbourhood can return results that are all nearby rather than in the region asked for. Pagination caps at 20 pages (about 820 listings) regardless of total matches, and relevance sort can drift between sessions, so use a deterministic sort like newest for parallel paging.

### How do I automatically search Zillow listings on zillow.com?

Ask an AI agent connected to Reduck to run reduck/zillow.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zillow.com/search

### Is there a zillow.com API to search Zillow listings?

You do not need one. "Search Zillow listings" drives the real zillow.com pages in a browser, so it works whether or not zillow.com offers an API for this.

### What information do I need to provide?

Required: location. Optional: page, sort, status, furnished.

### Do I need to be logged in to zillow.com?

No. It only uses pages of zillow.com that are reachable without signing in.

### Does it change anything on zillow.com, or only read data?

It only reads. It looks things up on zillow.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/zillow.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zillow.com/search

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/zillow.com/search
