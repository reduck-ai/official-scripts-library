# Search Zillow listings

Automatically search Zillow listings on zillow.com. One page of up to 41 homes for sale, for rent or sold, with price, beds, baths, square feet and map pin.

- Site: zillow.com
- Address: `reduck/zillow.com/search`
- Updated: 2026-10-06 (v17)
- Author: Reduck AI (reduck)

## About

Most people point this at one neighborhood and run it on a schedule instead of refreshing Zillow by hand. Say an investor watching 78704 in South Austin runs it every morning for homes for sale under $650,000, newest first (sort "days"), diffs the zpids against yesterday's run and pulls full details only for the new ones. The filters are the ones on Zillow's own filter bar, and switching status to recently_sold gives you the recent sales in a ZIP, which is where most comp checks start. On rentals and sold searches, an apartment building comes back as a single card with price, beds, baths and area all null; the per-unit numbers sit in units as Zillow's own strings, like "$2,150+" for a starting rent. When filters are tight, Zillow pads the page with listings from outside the area and marks them nearby:true. Drop those cards before you count anything.

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

## Output

- `region` (string | null, required): The place Zillow searched, as its search box shows it after the search (e.g. "Mission San Francisco CA", "San Francisco CA 94110"). Zillow never refuses a location: one it does not recognise is searched as the nearest place it does, with no error ("Mission District, San Francisco, CA" → "San Francisco CA"; "Nonexistentville, ZZ" → "Austin TX"). Compare it with what you asked for before treating the results as being in that place. Aliases are normal ("SoMa" → "South of Market San Francisco CA").
- `results` (array, required): The cards the site shows for this search, in the site's order: the in-boundary results first, then the relaxed (nearby) ones. Never empty: Zillow relaxes the boundary rather than showing nothing, so an empty array means a bucket of the answer went unread, not that the region is empty.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "region": "…",
  "results": [
    {
      "lat": "2026-01-15T09:30:00Z",
      "lng": 3.5,
      "area": 3.5,
      "beds": 3.5,
      "zpid": "…",
      "baths": 3.5,
      "price": 3.5,
      "units": [
        {
          "beds": "…",
          "price": "…",
          "roomForRent": true
        }
      ],
      "broker": "…",
      "imgSrc": "…",
      "nearby": true,
      "address": "…",
      "detailUrl": "https://example.com/item/123",
      "priceText": "…",
      "statusText": "…"
    }
  ]
}
```

## FAQ

### What does "Search Zillow listings" do?

Search Zillow listings for sale, for rent or recently sold in a location, with the site's own filters: price range, bedrooms, bathrooms, property type, furnished and space (rentals). Returns the place Zillow searched, as its search box shows it, and one page of cards with zpid, detailUrl, address, price, priceText, beds, baths, area, lat, lng, broker, imgSrc, statusText, units and nearby. Zillow searches the nearest place it knows when it does not recognise a location, so compare the returned place with the one you asked for. Apartment buildings come back as one card whose per-unit prices and bed counts are in units. When too few listings match inside the region, Zillow widens to the surrounding area; those cards have nearby:true. The site's result count includes every unit of a building, so a search can have fewer pages than that count suggests; a page past the last one fails. Pagination stops at 20 pages, and relevance order can change between sessions, so use a fixed sort such as newest when paging in parallel.

### How do I automatically search Zillow listings on zillow.com?

Ask an AI agent connected to Reduck to run reduck/zillow.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zillow.com/search

### Is there a zillow.com API to search Zillow listings?

You do not need one. "Search Zillow listings" drives the real zillow.com pages in a browser, so it works whether or not zillow.com offers an API for this.

### What information do I need to provide?

Required: location. Optional: page, sort, space, status, maxBeds, minBeds, maxPrice, minBaths, minPrice, furnished, homeTypes.

### What does it return?

It returns region, results.

### Do I need to be logged in to zillow.com?

No. It only uses pages of zillow.com that are reachable without signing in.

### Does it change anything on zillow.com, or only read data?

It only reads. It looks things up on zillow.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/zillow.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zillow.com/search

### Who maintains it?

It is part of Reduck's official curated catalogue.

### How many Zillow listings can one search return?

Zillow serves 41 homes per page and stops at 20 pages, which caps a single search at about 820 listings; to cover more, split the area by ZIP or by price band. Expect fewer pages than Zillow's headline count divided by 41, because that count includes every unit in an apartment building. If you fetch several pages at once, sort by "days" (newest first), since the default relevance order can shuffle between runs and hand you the same home twice.

### Does this Zillow search return the Zestimate?

No, the search output has no Zestimate field. Pass each zpid to the get_listing script for zillow.com to get the Zestimate along with year built, lot size, the description and rental details such as allowed pets and lease term. Zillow Group's own Zestimates API is aimed at businesses with a commercial use case, and access is granted on request.

### Why does a Zillow search sometimes fail with a Press & Hold error?

Press & Hold is Zillow's bot check. When it won't let the browser through, the run fails with an error naming that gate instead of returning an empty list that looks like nothing matched. The check shows up more when many searches start at the same moment, and on the sibling get_listing script it refused every run from Reduck's hosted cloud browser while almost all runs through the extension in a normal Chrome completed.

### What if Zillow doesn't recognize the location I give it?

Zillow quietly swaps an unknown place name for some default region (a made-up town once came back as Austin, TX), and the script fails when no word of three or more letters from your location appears in the region Zillow picked. Two-letter state codes are ignored, though: if Zillow mapped "Portland, ME" to Portland, OR, the check would not catch it. A bare ZIP skips the check entirely, which is why it pays to glance at the addresses on the first few cards whatever you searched for.

Source: https://reduck.ai/explore/scripts/reduck/zillow.com/search
