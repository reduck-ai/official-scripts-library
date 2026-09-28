# Search Zillow listings

Automatically search Zillow listings on zillow.com. Search Zillow listings for sale, for rent or recently sold in a location, with the site's own filters: price range, bedrooms, bathrooms, property type, furnished and space (rentals). Returns one page of cards with zpid, detailUrl, address, price, priceText, beds, baths, area, lat, lng, broker, imgSrc, statusText, units and nearby. Apartment buildings come back as one card whose per-unit prices and bed counts are in units. When too few listings match inside the region, Zillow widens to the surrounding area; those cards have nearby:true. The site's result count includes every unit of a building, so a search can have fewer pages than that count suggests; a page past the last one fails. Pagination stops at 20 pages, and relevance order can change between sessions, so use a fixed sort such as newest when paging in parallel.

- Site: zillow.com
- Address: `reduck/zillow.com/search`
- Updated: 2026-09-27 (v16)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/zillow.com/search`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/zillow.com/search
```

## Input

- `location` (string, required): A human-readable location: city+state ("Austin, TX"), a ZIP code ("90210"), or a neighborhood. The path form resolves it to a Zillow region server-side.
- `page` (integer, optional): 1-based result page (up to 41 cards each). Default 1. Zillow caps pagination at 20 pages (~820 listings) regardless of total matches. The site's "N rentals available" counts every unit of a building, so a search can have fewer pages than N/41; when fewer than 41 cards come back, it is the last page. A page past the last one throws.
- `sort` (string, optional): Sort order. Default "globalrelevanceex" (Homes for You) matches the site. When paging across independent browsers at the same time, pass a deterministic sort (e.g. "days" = newest) so pages partition identically — the default relevance order can drift between sessions.
- `space` (string, optional): The site's Space filter, rentals only. Omit for the site's default, "entire_place"; "room" = rooms for rent only; "any" = both.
- `status` (string, optional): Which Zillow listing category to search — the site's own For sale / For rent / Sold toggle, passed as its URL path segment. Default "for_sale". For-rent and recently-sold results include multi-unit building cards, which have no single price/beds/baths/area — those fields are null and the per-unit numbers are in `units` instead.
- `maxBeds` (integer, optional): Upper bedroom bound. Pass the same value as minBeds for the site's "Use exact match".
- `minBeds` (integer, optional): The site's Bedrooms filter ("2+"). 0 = studio.
- `maxPrice` (integer, optional): The site's Price filter, upper bound in USD. Monthly rent when status is for_rent, list price otherwise. Zillow matches a multi-unit building when at least one of its units falls in range, so its card can still show units above this.
- `minBaths` (number, optional): The site's Bathrooms filter: 1, 1.5, 2, 3 or 4 ("1.5+").
- `minPrice` (integer, optional): The site's Price filter, lower bound in USD. Monthly rent when status is for_rent, list price otherwise.
- `furnished` (boolean, optional): Restrict to Zillow's own "Furnished" rental filter. Only meaningful when status is for_rent — ignored for sale/sold listings. Default false = no restriction (all listings, furnished or not).
- `homeTypes` (array, optional): The site's Property type filter; omit for all types. For rent it offers houses, townhomes and apartments_condos. For sale and sold it offers houses, townhomes, multi_family, condos, lots_land, apartments and manufactured. A type the chosen status does not offer throws.

## FAQ

### What does "Search Zillow listings" do?

Search Zillow listings for sale, for rent or recently sold in a location, with the site's own filters: price range, bedrooms, bathrooms, property type, furnished and space (rentals). Returns one page of cards with zpid, detailUrl, address, price, priceText, beds, baths, area, lat, lng, broker, imgSrc, statusText, units and nearby. Apartment buildings come back as one card whose per-unit prices and bed counts are in units. When too few listings match inside the region, Zillow widens to the surrounding area; those cards have nearby:true. The site's result count includes every unit of a building, so a search can have fewer pages than that count suggests; a page past the last one fails. Pagination stops at 20 pages, and relevance order can change between sessions, so use a fixed sort such as newest when paging in parallel.

### How do I automatically search Zillow listings on zillow.com?

Ask an AI agent connected to Reduck to run reduck/zillow.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zillow.com/search

### Is there a zillow.com API to search Zillow listings?

You do not need one. "Search Zillow listings" drives the real zillow.com pages in a browser, so it works whether or not zillow.com offers an API for this.

### What information do I need to provide?

Required: location. Optional: page, sort, space, status, maxBeds, minBeds, maxPrice, minBaths, minPrice, furnished, homeTypes.

### Do I need to be logged in to zillow.com?

No. It only uses pages of zillow.com that are reachable without signing in.

### Does it change anything on zillow.com, or only read data?

It only reads. It looks things up on zillow.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/zillow.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zillow.com/search

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/zillow.com/search
