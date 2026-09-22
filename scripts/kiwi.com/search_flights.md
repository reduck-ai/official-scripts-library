# Search Kiwi flights

Automatically search Kiwi flights on kiwi.com. Search one-way flights on Kiwi for a given origin, destination, and date. One-way only; results are the visible flight cards (capped by max), not the full result set. Returns departure, arrival, duration, airline, origin, destination, stops, price, currency.

- Site: kiwi.com
- Address: `reduck/kiwi.com/search_flights`
- Updated: 2026-08-31 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kiwi.com/search_flights`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kiwi.com/search_flights
```

## Input

- `date` (string, required): Departure date, ISO YYYY-MM-DD (one-way only).
- `origin` (string, required): Origin city or airport typed into Kiwi's origin field (e.g. 'Paris' or 'CDG'). Ambiguous city names (e.g. multiple 'London's worldwide) are resolved automatically to the most relevant match.
- `destination` (string, required): Destination city or airport (e.g. 'London' or 'LON'). Ambiguous city names (e.g. multiple 'London's worldwide) are resolved automatically to the most relevant match.
- `max` (integer, optional): Max flight cards to return. Default 10.

## FAQ

### What does "Search Kiwi flights" do?

Search one-way flights on Kiwi for a given origin, destination, and date. One-way only; results are the visible flight cards (capped by max), not the full result set. Returns departure, arrival, duration, airline, origin, destination, stops, price, currency.

### How do I automatically search Kiwi flights on kiwi.com?

Ask an AI agent connected to Reduck to run reduck/kiwi.com/search_flights, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kiwi.com/search_flights

### Is there a kiwi.com API to search Kiwi flights?

You do not need one. "Search Kiwi flights" drives the real kiwi.com pages in a browser, so it works whether or not kiwi.com offers an API for this.

### What information do I need to provide?

Required: origin, destination, date. Optional: max.

### Do I need to be logged in to kiwi.com?

No. It only uses pages of kiwi.com that are reachable without signing in.

### Does it change anything on kiwi.com, or only read data?

It only reads. It looks things up on kiwi.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kiwi.com/search_flights, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kiwi.com/search_flights

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/kiwi.com/search_flights
