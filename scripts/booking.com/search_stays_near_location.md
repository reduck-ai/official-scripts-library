# Search stays near a location

Automatically search stays near a location on booking.com. Search Booking.com stays (hotels, apartments...) sorted by distance from a free-text location (address, landmark, city, hotel name), returning rating, distance, price and cancellation info per result.

- Site: booking.com
- Address: `reduck/booking.com/search_stays_near_location`
- Updated: 2026-09-25 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/booking.com/search_stays_near_location`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/booking.com/search_stays_near_location
```

## Input

- `checkin` (string, required): Check-in date, YYYY-MM-DD.
- `checkout` (string, required): Check-out date, YYYY-MM-DD.
- `location` (string, required): Free-text place to search near: address, landmark, city or hotel name (e.g. "124 Rue Réaumur, Paris" or "Tour Eiffel"). It must name a place Booking.com can actually find. Booking never answers "no match" — it quietly falls back to the nearest thing it can geocode anywhere in the world — so when the place it settles on shares nothing with what was asked, the search is refused instead of returning hotels somewhere else entirely.
- `rooms` (integer, optional): Number of rooms.
- `adults` (integer, optional): Number of adults.
- `children` (integer, optional): Number of children.
- `minRating` (number, optional): Only keep results with a review score at or above this threshold (0-10 scale). Properties with no reviews yet are excluded. Set to 0 to disable filtering.

## Output

- `results` (array, required)
- `resolvedLocation` (object, optional)
- `totalPropertiesFound` (integer | null, optional)

## FAQ

### What does "Search stays near a location" do?

Search Booking.com stays (hotels, apartments...) sorted by distance from a free-text location (address, landmark, city, hotel name), returning rating, distance, price and cancellation info per result.

### How do I automatically search stays near a location on booking.com?

Ask an AI agent connected to Reduck to run reduck/booking.com/search_stays_near_location, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/booking.com/search_stays_near_location

### Is there a booking.com API to search stays near a location?

You do not need one. "Search stays near a location" drives the real booking.com pages in a browser, so it works whether or not booking.com offers an API for this.

### What information do I need to provide?

Required: location, checkin, checkout. Optional: rooms, adults, children, minRating.

### What does it return?

It returns results, resolvedLocation, totalPropertiesFound.

### Do I need to be logged in to booking.com?

No. It only uses pages of booking.com that are reachable without signing in.

### Does it change anything on booking.com, or only read data?

It only reads. It looks things up on booking.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/booking.com/search_stays_near_location, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/booking.com/search_stays_near_location

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/booking.com/search_stays_near_location
