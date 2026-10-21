# Search Kiwi flights

Automatically search Kiwi flights on kiwi.com. Search one-way flights on Kiwi.com between two places on a date. Origin and destination are Kiwi place slugs; get them from kiwi.com/suggest_places. Returns up to 10 itineraries in Kiwi's Best order, each with local departure and arrival times, airport codes, duration, stops, airlines and price, plus the currency and Kiwi's total count of itineraries. Fails with a clear error when Kiwi does not recognise a place.

- Site: kiwi.com
- Address: `reduck/kiwi.com/search_flights`
- Updated: 2026-10-20 (v19)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kiwi.com/search_flights`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kiwi.com/search_flights
```

## Input

- `date` (string, required): Departure date, YYYY-MM-DD. One-way only.
- `origin` (string, required): Kiwi place slug of the departure city or airport, e.g. 'paris-france' or 'charles-de-gaulle-paris-france'. Get it from kiwi.com/suggest_places.
- `destination` (string, required): Kiwi place slug of the arrival city or airport, e.g. 'barcelona-spain'. Get it from kiwi.com/suggest_places.
- `max` (integer, optional): How many itineraries to return, in Kiwi's 'Best' order. Kiwi sends 10 at a time; total says how many exist.

## Output

- `total` (integer | null, required): How many itineraries Kiwi found in all.
- `currency` (string | null, required): Currency of every price, as Kiwi priced the search (ISO code, e.g. EUR).
- `itineraries` (array, required)

## FAQ

### What does "Search Kiwi flights" do?

Search one-way flights on Kiwi.com between two places on a date. Origin and destination are Kiwi place slugs; get them from kiwi.com/suggest_places. Returns up to 10 itineraries in Kiwi's Best order, each with local departure and arrival times, airport codes, duration, stops, airlines and price, plus the currency and Kiwi's total count of itineraries. Fails with a clear error when Kiwi does not recognise a place.

### How do I automatically search Kiwi flights on kiwi.com?

Ask an AI agent connected to Reduck to run reduck/kiwi.com/search_flights, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kiwi.com/search_flights

### Is there a kiwi.com API to search Kiwi flights?

You do not need one. "Search Kiwi flights" drives the real kiwi.com pages in a browser, so it works whether or not kiwi.com offers an API for this.

### What information do I need to provide?

Required: origin, destination, date. Optional: max.

### What does it return?

It returns total, currency, itineraries.

### Do I need to be logged in to kiwi.com?

No. It only uses pages of kiwi.com that are reachable without signing in.

### Does it change anything on kiwi.com, or only read data?

It only reads. It looks things up on kiwi.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kiwi.com/search_flights, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kiwi.com/search_flights

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/kiwi.com/search_flights
