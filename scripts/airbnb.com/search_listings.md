# Search Airbnb listings

Automatically search Airbnb listings on airbnb.com. Each stay comes back as a row with its price, rating, review count, coordinates and room link.

- Site: airbnb.com
- Address: `reduck/airbnb.com/search_listings`
- Updated: 2026-10-06 (v7)
- Author: Reduck AI (reduck)

## About

Handy when you want Airbnb results as rows you can sort instead of pins on a map. Say you rent out a two-bedroom flat in Alfama and want to price the first weekend of December. Search "Alfama, Lisbon" for 4 to 6 December with air conditioning and a kitchen required (amenity ids 5 and 8), and the flats nearby come back with the price Airbnb shows for those nights, the struck-through price if discounted, bedroom count, rating and coordinates. Sticking to the neighborhood rather than all of Lisbon keeps the list to flats a guest would weigh against yours. Leave the dates out and bedroom counts give way to each flat's next free dates. Prices arrive as text, often a whole phrase, in the language and currency Airbnb serves that browser (a browser in France lands on airbnb.fr, and a currency saved in its Airbnb settings counts too), so pull the number out before averaging.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/airbnb.com/search_listings`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/airbnb.com/search_listings
```

## Input

- `location` (string, required): Destination (city / region / neighborhood), e.g. 'Paris' or 'Lisbon, Portugal'. Spaces become dashes in the URL slug.
- `page` (integer, optional): Result page (up to 18 listings/page; Airbnb caps at ~15 pages). Default 1.
- `pets` (integer, optional): Number of pets.
- `query` (string, optional): Extra free-text query refinement.
- `adults` (integer, optional): Number of adults. Default 2.
- `checkin` (string, optional): Check-in date ISO YYYY-MM-DD. Pair with checkout for date-aware results/pricing.
- `infants` (integer, optional): Number of infants.
- `checkout` (string, optional): Check-out date ISO YYYY-MM-DD.
- `children` (integer, optional): Number of children.
- `amenities` (array, optional): Airbnb amenity-filter ids (the site's own filter pills), AND-combined as &amenities[]=<id>. Ids are sparse/non-sequential — common ones: 5=Air conditioning, 4=Wifi, 8=Kitchen, 9=Free parking, 7=Pool, 25=Hot tub, 30=Heating, 33=Washer, 34=Dryer, 58=TV, 51=Self check-in, 47=Dedicated workspace, 15=Gym, 16=Breakfast, 99=BBQ grill, 97=EV charger, 286=Crib, 45=Hair dryer, 46=Iron, 11=Smoking allowed, 27=Indoor fireplace, 35=Smoke alarm, 36=Carbon monoxide alarm.
- `category_tag` (string, optional): Airbnb category tag filter (e.g. 'Tag:8225').
- `titleStartsWith` (string, optional): Client-side filter: keep only listings whose title starts with this string.
- `l2_property_type_id` (integer | string, optional): Property-type filter id.

## Output

- `url` (string, required)
- `page` (integer, required)
- `count` (integer, required)
- `listings` (array, required)
- `maxPage` (integer | null, optional)
- `resolvedLocation` (object, optional): The place Airbnb actually searched. precision is "city" for a city, "state" for a region, "country" when Airbnb could only place the name at country level (the listings then cover the whole country), "building" for an address.

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

Search Airbnb stays for a location and date range. Returns url, page, count, maxPage, and listings (each with id, url, title, name, subtitle, lat, lng, rating, reviewCount, price, originalPrice, badges, details, hostType, imageUrl). One page returns up to 18 listings and Airbnb caps results at roughly 15 pages; paginate via the page arg.

### How do I automatically search Airbnb listings on airbnb.com?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/search_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/search_listings

### Is there a airbnb.com API to search Airbnb listings?

You do not need one. "Search Airbnb listings" drives the real airbnb.com pages in a browser, so it works whether or not airbnb.com offers an API for this.

### What information do I need to provide?

Required: location. Optional: page, pets, query, adults, checkin, infants, checkout, children, amenities, category_tag, titleStartsWith, l2_property_type_id.

### What does it return?

It returns url, page, count, maxPage, listings, resolvedLocation.

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
