# Kayak round-trip flight search

Search round-trip flights on Kayak.fr with free-text origin/destination city names and dates. Matches each city to its airport and returns price_eur (round-trip total), airline(s), duration, stops and layover text. Ad and promo cards (car rental, etc.) are excluded. An unresolvable city name returns noResults:true.

- Site: kayak.fr
- Address: `reduck/kayak.fr/search_flights_roundtrip`
- Updated: 2026-09-14 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kayak.fr/search_flights_roundtrip`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kayak.fr/search_flights_roundtrip
```

## Input

- `origin` (string, required): Origin city or airport, free text (e.g. 'Lyon' or 'Paris'). An IATA code (e.g. 'BCN') resolves unambiguously and is the way to bypass a cross-country name collision.
- `depart_date` (string, required): Outbound date, ISO YYYY-MM-DD.
- `destination` (string, required): Destination city or airport, free text (e.g. 'Lisbon'). An IATA code (e.g. 'BCN') resolves unambiguously and is the way to bypass a cross-country name collision.
- `return_date` (string, required): Return date, ISO YYYY-MM-DD (must be after depart_date).
- `max` (integer, optional): Max outbound options to return.

## Output

- `flights` (array, required)
- `noResults` (boolean, required): True when origin or destination free text didn't resolve to any airport via Kayak's autocomplete.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "flights": [
    {
      "stops": 3,
      "origin": "…",
      "airline": "…",
      "arrival": "…",
      "layover": "…",
      "duration": "…",
      "departure": "…",
      "price_eur": 3,
      "destination": "…"
    }
  ],
  "noResults": true
}
```

## FAQ

### What does "Kayak round-trip flight search" do?

Search round-trip flights on Kayak.fr with free-text origin/destination city names and dates. Matches each city to its airport and returns price_eur (round-trip total), airline(s), duration, stops and layover text. Ad and promo cards (car rental, etc.) are excluded. An unresolvable city name returns noResults:true.

### What information do I need to provide?

Required: origin, destination, depart_date, return_date. Optional: max.

### What does it return?

It returns flights, noResults.

### Do I need to be logged in to kayak.fr?

No. It only uses pages of kayak.fr that are reachable without signing in.

### Does it change anything on kayak.fr, or only read data?

It only reads. It looks things up on kayak.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kayak.fr/search_flights_roundtrip, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kayak.fr/search_flights_roundtrip

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Is there a Kayak API to search round-trip flights and prices?

Not an official one you can use for this: Kayak has no public flight-search API; its data is only open to affiliates. This script works as an unofficial Kayak API for it: typed input, JSON output, callable from an AI agent over MCP, from the CLI, or over REST.

### How do I search round-trip flights and prices programmatically?

Call this script with its arguments and read the JSON it returns. It drives Kayak in a real browser session, so there is no API key to request and nothing to reverse-engineer yourself.

Source: https://reduck.ai/explore/scripts/reduck/kayak.fr/search_flights_roundtrip
