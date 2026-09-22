# Google Flights round-trip search

Search round-trip flights on Google Flights from an explicit origin and destination (free text or IATA). Returns the outbound options with their total round-trip price (EUR), airline, duration, stops and layover. Each price is the round-trip total for that option; only the flights shown in the list are returned, and an unresolvable route returns noResults:true.

- Site: google.com
- Address: `reduck/google.com/search_flights_roundtrip`
- Updated: 2026-08-26 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/search_flights_roundtrip`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/search_flights_roundtrip
```

## Input

- `origin` (string, required): Origin city or airport, free text or IATA (e.g. 'Paris' or 'CDG').
- `depart_date` (string, required): Outbound date, ISO YYYY-MM-DD.
- `destination` (string, required): Destination city or airport, free text or IATA (e.g. 'Tokyo' or 'NRT').
- `return_date` (string, required): Return date, ISO YYYY-MM-DD (must be after depart_date).
- `max` (integer, optional): Max outbound options to return. Price-less rows are skipped so fewer may come back.

## Output

- `flights` (array, required)
- `noResults` (boolean, required): True when Google Flights could not resolve the route (lands on the empty search splash).

## FAQ

### What does "Google Flights round-trip search" do?

Search round-trip flights on Google Flights from an explicit origin and destination (free text or IATA). Returns the outbound options with their total round-trip price (EUR), airline, duration, stops and layover. Each price is the round-trip total for that option; only the flights shown in the list are returned, and an unresolvable route returns noResults:true.

### What information do I need to provide?

Required: origin, destination, depart_date, return_date. Optional: max.

### What does it return?

It returns flights, noResults.

### Do I need to be logged in to google.com?

No. It only uses pages of google.com that are reachable without signing in.

### Does it change anything on google.com, or only read data?

Unknown: its author has not declared whether it changes anything on google.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/search_flights_roundtrip, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/search_flights_roundtrip

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/search_flights_roundtrip
