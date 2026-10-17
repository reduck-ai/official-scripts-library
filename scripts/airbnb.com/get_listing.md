# Get Airbnb listing

Automatically get Airbnb listing on airbnb.com. Get one Airbnb listing by room id: name, property and room type, capacity, ratings and per-category ratings, host, photos, description, sleeping arrangement, amenities (with the ones not included), things to know (house rules, safety, cancellation summary), location, and the 12-month availability calendar, every day with its available flag and minimum stay. With checkin and checkout it also returns the booking quote for those dates and guests (price lines and total, or available false with Airbnb's reason) and the cancellation policy's refund milestones. Airbnb opens calendars about 12 months ahead; dates beyond that fail with an error that says so. Prices are in the currency you ask for (USD by default). A listing that does not exist or was removed fails with an error that says so.

- Site: airbnb.com
- Address: `reduck/airbnb.com/get_listing`
- Updated: 2026-10-16 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/airbnb.com/get_listing`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/airbnb.com/get_listing
```

## Input

- `id` (string, required): Airbnb room id, the number in /rooms/<id> (search_listings returns it).
- `pets` (integer, optional): Number of pets.
- `adults` (integer, optional): Number of adults. Default 2.
- `checkin` (string, optional): Check-in date, YYYY-MM-DD. With checkout, the result carries the quote and the cancellation policy for these dates. Airbnb opens its calendars about 12 months ahead.
- `infants` (integer, optional): Number of infants (under 2).
- `checkout` (string, optional): Check-out date, YYYY-MM-DD.
- `children` (integer, optional): Number of children (2-12).
- `currency` (string, optional): ISO 4217 currency for prices, e.g. USD or EUR. Default USD.

## Output

- `id` (string, required)
- `url` (string, required)
- `name` (string | null, required): The listing's own name, as its host wrote it.
- `quote` (object | null, required): The booking quote for the dates and guests asked for. Null without dates. available is false when the listing cannot be booked for them, with Airbnb's reason code (e.g. DATE); lines and total are then empty.
- `title` (string | null, required): Airbnb's summary line, e.g. "Rental unit in Lisbon · ★4.88 · 1 bedroom · 2 beds · 1 bath".
- `images` (array, required)
- `amenities` (array, required): Every amenity the listing page lists, available or not (the group "Not included" lists the ones it lacks).
- `availability` (array, required): The calendar the page loads: 12 months from the current one, day by day.
- `thingsToKnow` (array, required): The things-to-know blocks: type is Airbnb's own code (HOUSE_RULES, SAFETY_AND_PROPERTY, CANCELLATION_POLICY, INSTANT_BOOK...), items are the lines the page shows.
- `cancellationPolicy` (object | null, required): The refund milestones for the dates asked for. Null without dates: Airbnb gives them only for dates.
- `lat` (number | null, optional)
- `lng` (number | null, optional)
- `host` (object | null, optional)
- `rating` (number | null, optional)
- `roomType` (string | null, optional): Entire home/apt, Private room, Shared room or Hotel room.
- `sleeping` (array, optional)
- `description` (string | null, optional)
- `reviewCount` (integer | null, optional)
- `propertyType` (string | null, optional)
- `personCapacity` (integer | null, optional)
- `categoryRatings` (object, optional)
- `locationSubtitle` (string | null, optional): The place line of the location section, e.g. "Lisbon, Portugal".

## FAQ

### What does "Get Airbnb listing" do?

Get one Airbnb listing by room id: name, property and room type, capacity, ratings and per-category ratings, host, photos, description, sleeping arrangement, amenities (with the ones not included), things to know (house rules, safety, cancellation summary), location, and the 12-month availability calendar, every day with its available flag and minimum stay. With checkin and checkout it also returns the booking quote for those dates and guests (price lines and total, or available false with Airbnb's reason) and the cancellation policy's refund milestones. Airbnb opens calendars about 12 months ahead; dates beyond that fail with an error that says so. Prices are in the currency you ask for (USD by default). A listing that does not exist or was removed fails with an error that says so.

### How do I automatically get Airbnb listing on airbnb.com?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/get_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/get_listing

### Is there a airbnb.com API to get Airbnb listing?

You do not need one. "Get Airbnb listing" drives the real airbnb.com pages in a browser, so it works whether or not airbnb.com offers an API for this.

### What information do I need to provide?

Required: id. Optional: pets, adults, checkin, infants, checkout, children, currency.

### What does it return?

It returns id, lat, lng, url, host, name, quote, title, images, rating, roomType, sleeping, amenities, description, reviewCount, availability, propertyType, thingsToKnow, personCapacity, categoryRatings, locationSubtitle, cancellationPolicy.

### Do I need to be logged in to airbnb.com?

No. It only uses pages of airbnb.com that are reachable without signing in.

### Does it change anything on airbnb.com, or only read data?

It only reads. It looks things up on airbnb.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/get_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/get_listing

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/airbnb.com/get_listing
