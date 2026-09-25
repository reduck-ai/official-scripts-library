# Search Google flights

Automatically search Google flights on google.com. Search one-way flights on Google Flights. Returns a list of departure, arrival, airline, duration, origin, destination, stops, and price_eur. One-way only; price-less rows are skipped, so fewer than max may return; airline parsing is best-effort and can be null.

- Site: google.com
- Address: `reduck/google.com/search_flights`
- Updated: 2026-09-24 (v20)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/search_flights`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/search_flights
```

## Input

- `date` (string, required): Departure date, ISO YYYY-MM-DD (one-way only).
- `destination` (string, required): Destination city or airport, free text typed into Google Flights' 'Where to?' field (e.g. 'Tokyo' or 'NRT').
- `max` (integer, optional): Max flight rows to return. Default 10; price-less rows are skipped so fewer may come back.

## FAQ

### What does "Search Google flights" do?

Search one-way flights on Google Flights. Returns a list of departure, arrival, airline, duration, origin, destination, stops, and price_eur. One-way only; price-less rows are skipped, so fewer than max may return; airline parsing is best-effort and can be null.

### How do I automatically search Google flights on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/search_flights, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/search_flights

### Is there a google.com API to search Google flights?

You do not need one. "Search Google flights" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Required: destination, date. Optional: max.

### Do I need to be logged in to google.com?

No. It only uses pages of google.com that are reachable without signing in.

### Does it change anything on google.com, or only read data?

It only reads. It looks things up on google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/search_flights, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/search_flights

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/search_flights
