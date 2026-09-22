# Get Booking.com hotel details

Automatically get Booking.com hotel details on booking.com. Fetch a hotel's Booking.com listing: name, star rating, guest rating, review count, address, description, and image. No login required.

- Site: booking.com
- Address: `reduck/booking.com/get_hotel`
- Updated: 2026-09-02 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/booking.com/get_hotel`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/booking.com/get_hotel
```

## Input

- `hotel_slug` (string, required): Booking.com hotel path segment, e.g. "fr/hotelauroremontmartre" from booking.com/hotel/fr/hotelauroremontmartre.en-gb.html

## Output

- `available` (boolean, required)
- `hotel_slug` (string, required)
- `url` (string | null, optional)
- `name` (string | null, optional)
- `imageUrl` (string | null, optional)
- `postalCode` (string | null, optional)
- `starRating` (integer | null, optional)
- `description` (string | null, optional)
- `reviewCount` (integer | null, optional)
- `addressRegion` (string | null, optional)
- `streetAddress` (string | null, optional)
- `addressCountry` (string | null, optional)
- `addressLocality` (string | null, optional)
- `guestRatingBest` (number | null, optional)
- `guestRatingValue` (number | null, optional)

## FAQ

### What does "Get Booking.com hotel details" do?

Fetch a hotel's Booking.com listing: name, star rating, guest rating, review count, address, description, and image. No login required.

### How do I automatically get Booking.com hotel details on booking.com?

Ask an AI agent connected to Reduck to run reduck/booking.com/get_hotel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/booking.com/get_hotel

### Is there a booking.com API to get Booking.com hotel details?

You do not need one. "Get Booking.com hotel details" drives the real booking.com pages in a browser, so it works whether or not booking.com offers an API for this.

### What information do I need to provide?

Required: hotel_slug.

### What does it return?

It returns url, name, imageUrl, available, hotel_slug, postalCode, starRating, description, reviewCount, addressRegion, streetAddress, addressCountry, addressLocality, guestRatingBest, guestRatingValue.

### Do I need to be logged in to booking.com?

No. It only uses pages of booking.com that are reachable without signing in.

### Does it change anything on booking.com, or only read data?

It only reads. It looks things up on booking.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/booking.com/get_hotel, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/booking.com/get_hotel

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/booking.com/get_hotel
