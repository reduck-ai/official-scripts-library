# Get Airbnb listing (+availability)

Automatically get Airbnb listing (+availability) on airbnb.com. Fetch one Airbnb listing by room id: title, propertyType, capacity, rating and per-category ratings, host, images, description, sleeping arrangement, house rules, location (lat/lng), and the month-by-month availability calendar (per-day available/minNights/checkin-checkout). The only_available arg trims the calendar to bookable days.

- Site: airbnb.com
- Address: `reduck/airbnb.com/get_listing`
- Updated: 2026-09-02 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/airbnb.com/get_listing`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/airbnb.com/get_listing
```

## Input

- `id` (string, required): Airbnb room id (numeric).
- `adults` (integer, optional): Number of adults. Default 2.
- `checkin` (string, optional): Check-in ISO YYYY-MM-DD. Pair with checkout. Sets the URL dates; availability is returned regardless.
- `checkout` (string, optional): Check-out ISO YYYY-MM-DD.
- `only_available` (boolean, optional): When true, the availability calendar includes only bookable days (drops blocked days and empty months) — much smaller output. Default false returns every day with its available flag.

## Output

- `id` (string, required)
- `url` (string, required)
- `availability` (array | null, required)
- `lat` (number | null, optional)
- `lng` (number | null, optional)
- `host` (any, optional)
- `title` (string | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional)
- `roomType` (string | null, optional)
- `sleeping` (array, optional)
- `houseRules` (array, optional)
- `description` (string | null, optional)
- `reviewCount` (number | null, optional)
- `propertyType` (string | null, optional)
- `personCapacity` (number | null, optional)
- `categoryRatings` (object, optional)
- `locationSummary` (string | null, optional)
- `metaDescription` (string | null, optional)
- `locationSubtitle` (string | null, optional)

## FAQ

### What does "Get Airbnb listing (+availability)" do?

Fetch one Airbnb listing by room id: title, propertyType, capacity, rating and per-category ratings, host, images, description, sleeping arrangement, house rules, location (lat/lng), and the month-by-month availability calendar (per-day available/minNights/checkin-checkout). The only_available arg trims the calendar to bookable days.

### How do I automatically get Airbnb listing (+availability) on airbnb.com?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/get_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/get_listing

### Is there a airbnb.com API to get Airbnb listing (+availability)?

You do not need one. "Get Airbnb listing (+availability)" drives the real airbnb.com pages in a browser, so it works whether or not airbnb.com offers an API for this.

### What information do I need to provide?

Required: id. Optional: adults, checkin, checkout, only_available.

### What does it return?

It returns id, lat, lng, url, host, title, images, rating, roomType, sleeping, houseRules, description, reviewCount, availability, propertyType, personCapacity, categoryRatings, locationSummary, metaDescription, locationSubtitle.

### Do I need to be logged in to airbnb.com?

No. It only uses pages of airbnb.com that are reachable without signing in.

### Does it change anything on airbnb.com, or only read data?

It only reads. It looks things up on airbnb.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/get_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/get_listing

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/airbnb.com/get_listing
