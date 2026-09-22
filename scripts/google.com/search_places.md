# Search Google Maps places

Automatically search Google Maps places on google.com. Search Google Maps for places matching a query, optionally near a location. Returns n, captured, and records with name, address, phone, website, rating, category, lat, lng, placeId, and placeUrl. placeId is the join key for get_place and get_place_reviews; rating, category, lat and lng can be null.

- Site: google.com
- Address: `reduck/google.com/search_places`
- Updated: 2026-08-17 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/search_places`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/search_places
```

## Input

- `query` (string, required): Search terms (e.g. 'tatoueur', 'pizzeria', 'dentist near me').
- `gl` (string, optional): Geo region (e.g. 'fr', 'us'). Empty = Maps default.
- `hl` (string, optional): UI language (e.g. 'fr', 'en'). Empty = Maps default.
- `cap` (number, optional): Hard cap on returned records.
- `location` (string, optional): Optional location appended to the query (e.g. 'Paris', 'Brooklyn'). If empty, only `query` is used.
- `maxScrolls` (number, optional): Max scroll rounds before bailing on staleness.

## Output

- `n` (number, optional): Number of unique records returned.
- `records` (array, optional)
- `captured` (number, optional): Number of /search?tbm=map XHRs captured.

## FAQ

### What does "Search Google Maps places" do?

Search Google Maps for places matching a query, optionally near a location. Returns n, captured, and records with name, address, phone, website, rating, category, lat, lng, placeId, and placeUrl. placeId is the join key for get_place and get_place_reviews; rating, category, lat and lng can be null.

### How do I automatically search Google Maps places on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/search_places, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/search_places

### Is there a google.com API to search Google Maps places?

You do not need one. "Search Google Maps places" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: gl, hl, cap, location, maxScrolls.

### What does it return?

It returns n, records, captured.

### Do I need to be logged in to google.com?

No. It only uses pages of google.com that are reachable without signing in.

### Does it change anything on google.com, or only read data?

It only reads. It looks things up on google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/search_places, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/search_places

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/search_places
