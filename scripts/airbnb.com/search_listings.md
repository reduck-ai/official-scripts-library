# Search Airbnb listings

Automatically search Airbnb listings on airbnb.com. Search Airbnb stays for a location and date range. Returns url, page, count, maxPage, and listings (each with id, url, title, name, subtitle, lat, lng, rating, reviewCount, price, originalPrice, badges, details, hostType, imageUrl). One page returns up to 18 listings and Airbnb caps results at roughly 15 pages; paginate via the page arg.

- Site: airbnb.com
- Address: `reduck/airbnb.com/search_listings`
- Updated: 2026-09-02 (v6)
- Author: Reduck AI (reduck)

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

It returns url, page, count, maxPage, listings.

### Do I need to be logged in to airbnb.com?

No. It only uses pages of airbnb.com that are reachable without signing in.

### Does it change anything on airbnb.com, or only read data?

It only reads. It looks things up on airbnb.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/search_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/search_listings

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/airbnb.com/search_listings
