# Suggest Paris flight destinations

Automatically suggest Paris flight destinations on parisaeroport.fr. Resolve a free-text destination to Paris Aéroport's ranked airport suggestions [{iataCode, name, city, ...}] ([0] = best), as the site's own typeahead answers it on its English board. Disambiguates multi-airport cities; pass a returned name to search_departures. Pass the destination in English (e.g. "London"); names come back in English (LONDON GATWICK). An empty list means the site has no destination for that text.

- Site: parisaeroport.fr
- Address: `reduck/parisaeroport.fr/suggest_destinations`
- Updated: 2026-11-19 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/parisaeroport.fr/suggest_destinations`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/parisaeroport.fr/suggest_destinations
```

## Input

- `query` (string, required): Free-text destination to look up, in English, e.g. 'Shanghai', 'London', 'New York'. Matches the site's own typeahead on its English board.
- `limit` (integer, optional): Max suggestions to return.

## Output

- `query` (string, required)
- `matchedTerm` (string, required): The term the returned suggestions correspond to. Always equals `query`.
- `destinations` (array, required): Airport suggestions in the site's ranked order ([0] = best match). Empty when the site has no destination for the query. A metro (e.g. London) yields one entry per airport, sharing a cityCode.

## FAQ

### What does "Suggest Paris flight destinations" do?

Resolve a free-text destination to Paris Aéroport's ranked airport suggestions [{iataCode, name, city, ...}] ([0] = best), as the site's own typeahead answers it on its English board. Disambiguates multi-airport cities; pass a returned name to search_departures. Pass the destination in English (e.g. "London"); names come back in English (LONDON GATWICK). An empty list means the site has no destination for that text.

### How do I automatically suggest Paris flight destinations on parisaeroport.fr?

Ask an AI agent connected to Reduck to run reduck/parisaeroport.fr/suggest_destinations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/parisaeroport.fr/suggest_destinations

### Is there a parisaeroport.fr API to suggest Paris flight destinations?

You do not need one. "Suggest Paris flight destinations" drives the real parisaeroport.fr pages in a browser, so it works whether or not parisaeroport.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: limit.

### What does it return?

It returns query, matchedTerm, destinations.

### Do I need to be logged in to parisaeroport.fr?

No. It only uses pages of parisaeroport.fr that are reachable without signing in.

### Does it change anything on parisaeroport.fr, or only read data?

It only reads. It looks things up on parisaeroport.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/parisaeroport.fr/suggest_destinations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/parisaeroport.fr/suggest_destinations

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/parisaeroport.fr/suggest_destinations
