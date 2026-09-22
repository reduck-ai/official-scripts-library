# Search Booking.com hotels

Automatically search Booking.com hotels on booking.com. Search Booking.com for accommodations by destination: name, hotel slug, address, guest rating, review count, and rating category. No login required.

- Site: booking.com
- Address: `reduck/booking.com/search_hotels`
- Updated: 2026-09-02 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/booking.com/search_hotels`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/booking.com/search_hotels
```

## Input

- `destination` (string, required): Destination to search, e.g. "Rome" or "Paris"

## Output

- `results` (array, required)
- `destination` (string, required)

## FAQ

### What does "Search Booking.com hotels" do?

Search Booking.com for accommodations by destination: name, hotel slug, address, guest rating, review count, and rating category. No login required.

### How do I automatically search Booking.com hotels on booking.com?

Ask an AI agent connected to Reduck to run reduck/booking.com/search_hotels, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/booking.com/search_hotels

### Is there a booking.com API to search Booking.com hotels?

You do not need one. "Search Booking.com hotels" drives the real booking.com pages in a browser, so it works whether or not booking.com offers an API for this.

### What information do I need to provide?

Required: destination.

### What does it return?

It returns results, destination.

### Do I need to be logged in to booking.com?

No. It only uses pages of booking.com that are reachable without signing in.

### Does it change anything on booking.com, or only read data?

It only reads. It looks things up on booking.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/booking.com/search_hotels, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/booking.com/search_hotels

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/booking.com/search_hotels
