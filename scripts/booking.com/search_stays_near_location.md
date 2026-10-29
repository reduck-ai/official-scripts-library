# Search Booking.com stays near a location

Automatically search Booking.com stays near a location on booking.com. Search Booking.com stays (hotels, apartments...) sorted by distance from a free-text location (address, landmark, city, hotel name), returning rating, distance, price and cancellation info per result.

- Site: booking.com
- Address: `reduck/booking.com/search_stays_near_location`
- Updated: 2026-10-28 (v12)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/booking.com/search_stays_near_location`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/booking.com/search_stays_near_location
```

## Input

- `checkin` (string, required): Check-in date, YYYY-MM-DD.
- `checkout` (string, required): Check-out date, YYYY-MM-DD.
- `location` (string, required): Free-text place to search near: address, landmark, city or hotel name (e.g. "124 Rue Réaumur, Paris" or "Tour Eiffel"). It must name a place Booking.com can actually find. When several places share the name (e.g. "Paris"), the search is refused and the candidates are listed: add the country or region after a comma ("Paris, France"). Booking never answers "no match" — it quietly falls back to the nearest thing it can geocode anywhere in the world — so when the place it settles on shares nothing with what was asked, the search is refused instead of returning hotels somewhere else entirely. The place used is returned as resolvedLocation.
- `rooms` (integer, optional): Number of rooms.
- `adults` (integer, optional): Number of adults.
- `offset` (integer, optional): Index of the first result to return, for paging: 0 for the first page, then add resultsPerPage from the previous answer until offset reaches totalPropertiesFound.
- `children` (integer, optional): Number of children.

## Output

- `results` (array, required)
- `offset` (integer, optional): The offset this page starts at.
- `resultsPerPage` (integer | null, optional): How many results Booking.com puts on one page.
- `resolvedLocation` (object, optional)
- `totalPropertiesFound` (integer | null, optional): Total number of properties Booking.com found for the search, across all pages.

## FAQ

### What does "Search Booking.com stays near a location" do?

Search Booking.com stays (hotels, apartments...) sorted by distance from a free-text location (address, landmark, city, hotel name), returning rating, distance, price and cancellation info per result.

### How do I automatically search Booking.com stays near a location on booking.com?

Ask an AI agent connected to Reduck to run reduck/booking.com/search_stays_near_location, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/booking.com/search_stays_near_location

### Is there a booking.com API to search Booking.com stays near a location?

You do not need one. "Search Booking.com stays near a location" drives the real booking.com pages in a browser, so it works whether or not booking.com offers an API for this.

### What information do I need to provide?

Required: location, checkin, checkout. Optional: rooms, adults, offset, children.

### What does it return?

It returns offset, results, resultsPerPage, resolvedLocation, totalPropertiesFound.

### Do I need to be logged in to booking.com?

No. It only uses pages of booking.com that are reachable without signing in.

### Does it change anything on booking.com, or only read data?

It only reads. It looks things up on booking.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/booking.com/search_stays_near_location, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/booking.com/search_stays_near_location

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/booking.com/search_stays_near_location
