# Craigslist API: search Craigslist apartments for rent

Automatically search Craigslist apartments for rent on craigslist.org. An unofficial Craigslist API for apartment listings: search apartments, rooms and sublets for rent in any city, newest first, filtered by rent, bedrooms, pets and distance, as data in one call. Run it every few minutes to catch new listings first. Search Craigslist's housing-for-rent listings in any Craigslist city (the SF Bay Area by default, or one part of it such as San Francisco, East Bay or Peninsula), for whole apartments, rooms in shared homes, or sublets. Filter by keywords, rent, bedrooms, bathrooms, square feet, cats or dogs allowed, furnished, listings with photos, listings posted today, and distance from a ZIP code; sort by newest or by price. Each result gives the listing link, title, asking rent, neighborhood, city, bedrooms, bathrooms and map coordinates. One search returns up to the newest few hundred matches and says whether that is all of them; when it is not, narrow the filters to reach the rest. Pass a listing link to get_housing_listing for the full description, address, photos and amenities.

- Site: craigslist.org
- Address: `reduck/craigslist.org/search_housing`
- Updated: 2026-09-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/craigslist.org/search_housing`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/craigslist.org/search_housing
```

## Input

- `site` (string, optional): The Craigslist city, as its web address starts: sfbay (SF Bay Area), newyork, losangeles, seattle, boston, chicago…
- `sort` (string, optional)
- `query` (string, optional): Keywords, as typed in the site's search box.
- `catsOk` (boolean, optional): Only listings that allow cats.
- `dogsOk` (boolean, optional): Only listings that allow dogs.
- `maxSqft` (integer, optional)
- `minSqft` (integer, optional)
- `subarea` (string, optional): One part of the city's area, as Craigslist abbreviates it. For sfbay: sfc (San Francisco), eby (East Bay), pen (Peninsula), sby (South Bay), nby (North Bay), scz (Santa Cruz). Omit for the whole area.
- `category` (string, optional): apartments: whole units for rent. rooms: a room in a shared home. sublets: sublets and temporary stays.
- `hasImage` (boolean, optional): Only listings with photos.
- `maxPrice` (integer, optional): Maximum monthly rent, in the site's currency.
- `minPrice` (integer, optional): Minimum monthly rent, in the site's currency.
- `furnished` (boolean, optional): Only furnished listings.
- `postalCode` (string, optional): ZIP code to measure distance from; use with distanceMiles.
- `titlesOnly` (boolean, optional): Match the keywords against listing titles only.
- `maxBedrooms` (integer, optional)
- `minBedrooms` (integer, optional)
- `postedToday` (boolean, optional): Only listings posted today.
- `maxBathrooms` (number, optional)
- `minBathrooms` (number, optional)
- `distanceMiles` (number, optional): Only listings within this many miles of postalCode.

## Output

- `count` (integer, required)
- `total` (integer, required): How many listings match on the site, counting reposts of one listing that the site shows once.
- `complete` (boolean, required): true: every match is in listings. false: only the newest batch came back; narrow the filters to reach the rest.
- `listings` (array, required)
- `searchUrl` (string, required): The search page as the site resolved it.

## FAQ

### What does "Craigslist API: search Craigslist apartments for rent" do?

An unofficial Craigslist API for apartment listings: search apartments, rooms and sublets for rent in any city, newest first, filtered by rent, bedrooms, pets and distance, as data in one call. Run it every few minutes to catch new listings first. Search Craigslist's housing-for-rent listings in any Craigslist city (the SF Bay Area by default, or one part of it such as San Francisco, East Bay or Peninsula), for whole apartments, rooms in shared homes, or sublets. Filter by keywords, rent, bedrooms, bathrooms, square feet, cats or dogs allowed, furnished, listings with photos, listings posted today, and distance from a ZIP code; sort by newest or by price. Each result gives the listing link, title, asking rent, neighborhood, city, bedrooms, bathrooms and map coordinates. One search returns up to the newest few hundred matches and says whether that is all of them; when it is not, narrow the filters to reach the rest. Pass a listing link to get_housing_listing for the full description, address, photos and amenities.

### How do I automatically search Craigslist apartments for rent on craigslist.org?

Ask an AI agent connected to Reduck to run reduck/craigslist.org/search_housing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/craigslist.org/search_housing

### Is there a craigslist.org API to search Craigslist apartments for rent?

You do not need one. "Craigslist API: search Craigslist apartments for rent" drives the real craigslist.org pages in a browser, so it works whether or not craigslist.org offers an API for this.

### What information do I need to provide?

Optional: site, sort, query, catsOk, dogsOk, maxSqft, minSqft, subarea, category, hasImage, maxPrice, minPrice, furnished, postalCode, titlesOnly, maxBedrooms, minBedrooms, postedToday, maxBathrooms, minBathrooms, distanceMiles.

### What does it return?

It returns count, total, complete, listings, searchUrl.

### Do I need to be logged in to craigslist.org?

No. It only uses pages of craigslist.org that are reachable without signing in.

### Does it change anything on craigslist.org, or only read data?

It only reads. It looks things up on craigslist.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/craigslist.org/search_housing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/craigslist.org/search_housing

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/craigslist.org/search_housing
