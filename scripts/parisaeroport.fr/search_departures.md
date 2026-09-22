# Search Paris departures by destination

Automatically search Paris departures by destination on parisaeroport.fr. List today's upcoming departures from Paris (CDG/ORY) to a destination, with times, terminal, status, and codeshares — from the official Paris Aéroport flight search.

- Site: parisaeroport.fr
- Address: `reduck/parisaeroport.fr/search_departures`
- Updated: 2026-08-03 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/parisaeroport.fr/search_departures`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/parisaeroport.fr/search_departures
```

## Input

- `destination` (string, required): Free-text destination, e.g. 'Shanghai', 'London', 'New York'. Matched by the site's own typeahead at CITY level (also matches its French names, e.g. 'Londres'), so a multi-airport city returns flights to ALL its airports. To target one airport, filter the returned flights by arrivalIataCode (get the code from suggest_destinations).
- `airport` (string, optional): Paris airport filter, applied server-side: 'cdg' (Paris-CDG), 'ory' (Paris-ORY), or 'all' (both).

## Output

- `count` (integer, required)
- `airport` (string, required)
- `flights` (array, required)
- `destination` (string, required)

## FAQ

### What does "Search Paris departures by destination" do?

List today's upcoming departures from Paris (CDG/ORY) to a destination, with times, terminal, status, and codeshares — from the official Paris Aéroport flight search.

### How do I automatically search Paris departures by destination on parisaeroport.fr?

Ask an AI agent connected to Reduck to run reduck/parisaeroport.fr/search_departures, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/parisaeroport.fr/search_departures

### Is there a parisaeroport.fr API to search Paris departures by destination?

You do not need one. "Search Paris departures by destination" drives the real parisaeroport.fr pages in a browser, so it works whether or not parisaeroport.fr offers an API for this.

### What information do I need to provide?

Required: destination. Optional: airport.

### What does it return?

It returns count, airport, flights, destination.

### Do I need to be logged in to parisaeroport.fr?

No. It only uses pages of parisaeroport.fr that are reachable without signing in.

### Does it change anything on parisaeroport.fr, or only read data?

Unknown: its author has not declared whether it changes anything on parisaeroport.fr, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/parisaeroport.fr/search_departures, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/parisaeroport.fr/search_departures

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/parisaeroport.fr/search_departures
