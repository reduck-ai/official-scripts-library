# Check Berlin City Tour ticket availability for a date

Automatically check Berlin City Tour ticket availability for a date on berlin-city-tour.de. Reads the Berlin City Tour shop for one calendar date and returns the bookable timeslots, the per-guest-category prices, and the remaining capacity. The Hop-on Hop-off Classic tour is sold as a day ticket, so a bookable date has a single open timeslot covering the whole day rather than departure times. When the date is not on sale it returns available false with the reason the shop gave and the other dates on sale around it, so the caller can offer an alternative instead of guessing. The offer_hash it returns identifies the date, the slots and the prices it saw; pass it to add_to_cart, which refuses if the shop has changed since.

- Site: berlin-city-tour.de
- Address: `reduck/berlin-city-tour.de/check_availability`
- Updated: 2026-11-13 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/berlin-city-tour.de/check_availability`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/berlin-city-tour.de/check_availability
```

## Input

- `date` (string, required): The travel date to check, as YYYY-MM-DD.
- `nearbyDays` (integer, optional): How many days either side of the date to report as alternatives.
- `packageGroupId` (integer, optional): The product to check. 1137 is the Hop-on Hop-off Classic tour 24h.

## Output

- `date` (string, required)
- `slots` (array, required)
- `prices` (array, required)
- `available` (boolean, required)
- `offer_hash` (string, required)
- `packageGroupId` (integer, required)
- `nearbyAvailableDates` (array, required)
- `reason` (string | null, optional): Why the date is not bookable, when the shop said.
- `currency` (string | null, optional)
- `productName` (string | null, optional)

## FAQ

### What does "Check Berlin City Tour ticket availability for a date" do?

Reads the Berlin City Tour shop for one calendar date and returns the bookable timeslots, the per-guest-category prices, and the remaining capacity. The Hop-on Hop-off Classic tour is sold as a day ticket, so a bookable date has a single open timeslot covering the whole day rather than departure times. When the date is not on sale it returns available false with the reason the shop gave and the other dates on sale around it, so the caller can offer an alternative instead of guessing. The offer_hash it returns identifies the date, the slots and the prices it saw; pass it to add_to_cart, which refuses if the shop has changed since.

### How do I automatically check Berlin City Tour ticket availability for a date on berlin-city-tour.de?

Ask an AI agent connected to Reduck to run reduck/berlin-city-tour.de/check_availability, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/berlin-city-tour.de/check_availability

### Is there a berlin-city-tour.de API to check Berlin City Tour ticket availability for a date?

You do not need one. "Check Berlin City Tour ticket availability for a date" drives the real berlin-city-tour.de pages in a browser, so it works whether or not berlin-city-tour.de offers an API for this.

### What information do I need to provide?

Required: date. Optional: nearbyDays, packageGroupId.

### What does it return?

It returns date, slots, prices, reason, currency, available, offer_hash, productName, packageGroupId, nearbyAvailableDates.

### Do I need to be logged in to berlin-city-tour.de?

No. It only uses pages of berlin-city-tour.de that are reachable without signing in.

### Does it change anything on berlin-city-tour.de, or only read data?

It only reads. It looks things up on berlin-city-tour.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/berlin-city-tour.de/check_availability, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/berlin-city-tour.de/check_availability

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/berlin-city-tour.de/check_availability
