# Search Airbnb listings

Automatically search Airbnb listings on airbnb.com. Each stay comes back as a row with its price, rating, review count, coordinates and room link.

- Site: airbnb.com
- Address: `reduck/airbnb.com/search_listings`
- Updated: 2026-10-30 (v11)
- Author: Reduck AI (reduck)

## About

Handy when you want Airbnb results as rows you can sort instead of pins on a map. Say you rent out a two-bedroom flat in Alfama and want to price the first weekend of December. Search "Alfama, Lisbon" for 4 to 6 December with air conditioning and a kitchen required (amenity ids 5 and 8), and the flats nearby come back with the price Airbnb shows for those nights, the struck-through price if discounted, bedroom count, rating and coordinates. Sticking to the neighborhood rather than all of Lisbon keeps the list to flats a guest would weigh against yours. Leave the dates out and bedroom counts give way to each flat's next free dates. Prices arrive as text, often a whole phrase, in the language and currency Airbnb serves that browser (a browser in France lands on airbnb.fr, and a currency saved in its Airbnb settings counts too), so pull the number out before averaging.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/airbnb.com/search_listings`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/airbnb.com/search_listings
```

## Input

- `location` (string, required): Destination as a person types it: a city, a region or a neighborhood, e.g. "Paris" or "Lisbon, Portugal".
- `ib` (boolean, optional): Instant Book only.
- `page` (integer, optional): Result page, 18 listings each. Airbnb stops at about 15 pages: maxPage says how many this search has.
- `pets` (integer, optional): Number of pets; 1 or more keeps only listings that allow pets.
- `adults` (integer, optional): Number of adults. Default 2.
- `bounds` (object, optional): Search only inside this rectangle of the map, as moving Airbnb's map does: its north-east and south-west corners. location still names the city. Useful to stay near one address: take its coordinates (for example from google.com/get_place) and add a margin.
- `checkin` (string, optional): Check-in date, YYYY-MM-DD. With checkout, prices are for those dates.
- `infants` (integer, optional)
- `checkout` (string, optional): Check-out date, YYYY-MM-DD.
- `children` (integer, optional)
- `currency` (string, optional): ISO 4217 currency for prices. Default USD.
- `min_beds` (integer, optional)
- `tier_ids` (array, optional): Listing tiers, e.g. Luxe (values from list_search_filters).
- `amenities` (array, optional): Amenity ids, all required (values from list_search_filters, key amenities).
- `price_max` (integer, optional): Maximum price, in currency.
- `price_min` (integer, optional): Minimum price, in currency.
- `room_types` (array, optional): Room types, e.g. ["Entire home/apt"] or ["Private room"] (values from list_search_filters).
- `kg_and_tags` (array, optional): Property tags, e.g. hotel, beachfront (values from list_search_filters).
- `min_bedrooms` (integer, optional)
- `min_bathrooms` (integer, optional)
- `guest_favorite` (boolean, optional): Guest favorites only.
- `host_languages` (array, optional): Host language codes, e.g. ["fr"] (values from list_search_filters).
- `bathroom_privacy` (string, optional): e.g. "ENSUITE" for a private attached bathroom (values from list_search_filters).
- `neighborhood_ids` (array, optional): Neighborhood ids of this location (values from list_search_filters for the same location).
- `l2_property_type_ids` (array, optional): Property type ids, e.g. house or apartment (values from list_search_filters).

## Output

- `url` (string, required)
- `page` (integer, required)
- `count` (integer, required): Listings on this page.
- `listings` (array, required)
- `resolvedLocation` (object, required): The place Airbnb searched. precision is "city", "state" for a region, "country" when Airbnb could place the name only at country level (the listings then cover the whole country), "building" for an address.
- `maxPage` (integer | null, optional)
- `totalCount` (integer | null, optional): Listings the whole search matches, as Airbnb counts them.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "url": "https://example.com/item/123",
  "page": 1,
  "count": 3,
  "maxPage": 3,
  "listings": [
    {
      "id": "abc123",
      "lat": "2026-01-15T09:30:00Z",
      "lng": 3.5,
      "url": "https://example.com/item/123",
      "name": "Example",
      "price": "…",
      "title": "Example",
      "badges": [
        "…"
      ],
      "images": [
        "…"
      ],
      "rating": 3.5,
      "details": [
        "…"
      ],
      "hostType": "…",
      "imageUrl": "https://example.com/item/123",
      "subtitle": "…",
      "ratingLabel": "…",
      "reviewCount": 3,
      "availability": [
        "…"
      ],
      "originalPrice": "…",
      "priceQualifier": "…"
    }
  ],
  "totalCount": 3,
  "resolvedLocation": {
    "name": "Example",
    "bounds": {
      "northeast": {
        "lat": "2026-01-15T09:30:00Z",
        "lng": 3.5
      },
      "southwest": {
        "lat": "2026-01-15T09:30:00Z",
        "lng": 3.5
      }
    },
    "center": {
      "lat": "2026-01-15T09:30:00Z",
      "lng": 3.5
    },
    "precision": "…",
    "canonicalLocation": "…"
  }
}
```

## FAQ

### What does "Search Airbnb listings" do?

Search Airbnb stays in a location, with or without dates, with the filters Airbnb offers: guests, price range, room type, bedrooms, beds, bathrooms, Instant Book, guest favorites, amenities, property type, tags, host language and neighborhood (List Airbnb search filters gives their values). A map area (the north-east and south-west corners of a rectangle) limits the search to the listings inside it, as moving Airbnb's map does, for example around an office whose coordinates google.com/get_place gives. Returns one page of up to 18 listings (room id, name, price line, rating and review count, coordinates, badges, room details or next free dates, photos), the total count of matching listings, the number of pages (Airbnb stops at about 15) and the place Airbnb searched. A listing's coordinates feed google.com/get_directions for the trip to a place; Airbnb blurs them by a few hundred meters. A filter or a map area nothing matches returns an empty list. A location Airbnb cannot place fails with an error instead of returning its worldwide default list. Prices are in the currency you ask for (USD by default).

### How do I automatically search Airbnb listings on airbnb.com?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/search_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/search_listings

### Is there a airbnb.com API to search Airbnb listings?

You do not need one. "Search Airbnb listings" drives the real airbnb.com pages in a browser, so it works whether or not airbnb.com offers an API for this.

### What information do I need to provide?

Required: location. Optional: ib, page, pets, adults, bounds, checkin, infants, checkout, children, currency, min_beds, tier_ids, amenities, price_max, price_min, room_types, kg_and_tags, min_bedrooms, min_bathrooms, guest_favorite, host_languages, bathroom_privacy, neighborhood_ids, l2_property_type_ids.

### What does it return?

It returns url, page, count, maxPage, listings, totalCount, resolvedLocation.

### Do I need to be logged in to airbnb.com?

No. It only uses pages of airbnb.com that are reachable without signing in.

### Does it change anything on airbnb.com, or only read data?

It only reads. It looks things up on airbnb.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/search_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/search_listings

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can I find an Airbnb listing by its street address?

Airbnb keeps the street address hidden until a booking is confirmed, so no search result carries one, and the closest you can get is searching the neighborhood or city the address sits in, then comparing each result's photos and coordinates with the place you have in mind. Inside Airbnb reports that listing locations in Airbnb's data sit up to about 150 metres from the real address, so the lat and lng point to a block, not a door.

### How many Airbnb listings can one search return?

One Airbnb search tops out around 270 stays, 18 a page over roughly 15 pages, and the maxPage field (when Airbnb returns pagination) gives the page count for that particular search. Pages can be fetched in any order, so page 9 does not need pages 1 to 8 first. To cover a whole city, search it neighborhood by neighborhood, one search after another on the same browser rather than in parallel, and dedupe by listing id when you merge, since rankings shift between runs and neighboring areas overlap.

### Can I track one Airbnb listing from its link?

The number after /rooms/ in an Airbnb link is the room id, and Reduck's get_listing script for airbnb.com takes that id and returns the listing's day-by-day calendar with minimum nights, plus its house rules and per-category ratings. To follow prices across an area, rerun the same dated search on the same browser on a schedule and compare each id's price string between runs, which shows which listings entered or left the results and which prices moved.

### Can I filter Airbnb by amenities that are not in the filter panel?

Airbnb's filter panel shows only about two dozen amenities, but its search URLs accept several hundred numeric amenity codes through amenities[], according to the code list published by custombnb.app. The amenities input takes those same numbers and requires all of them at once, so [5, 51] keeps only stays with air conditioning and self check-in.

Source: https://reduck.ai/explore/scripts/reduck/airbnb.com/search_listings
