# Suggest Deutsche Bahn (bahn.de) stations and places

Automatically suggest Deutsche Bahn (bahn.de) stations and places on bahn.de. Look up stations, addresses and points of interest on Deutsche Bahn (bahn.de) by name, as its Start and Destination fields suggest them while you type, in bahn.de's own order (up to 10). Returns each place's id, name, type (station, address or point of interest), station number, coordinates and the kinds of transport that stop there. Pass a place's id to bahn.de/search_journeys as origin or destination. A city name in capitals, such as MUNICH (MÜNCHEN), stands for all the stations of that city. Names are in English where bahn.de has an English name, with the local name in brackets. bahn.de's matching is loose: a text it does not know still brings up places whose names start like it, so check the names before you search.

- Site: bahn.de
- Address: `reduck/bahn.de/suggest_locations`
- Updated: 2026-11-04 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bahn.de/suggest_locations`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bahn.de/suggest_locations
```

## Input

- `query` (string, required): A station, city, address or place name, as you would type it in bahn.de's Start field, e.g. 'Munich' or 'Paris Est'.

## Output

- `places` (array, required): bahn.de's suggestions, in its order. Empty when it has none.

## FAQ

### What does "Suggest Deutsche Bahn (bahn.de) stations and places" do?

Look up stations, addresses and points of interest on Deutsche Bahn (bahn.de) by name, as its Start and Destination fields suggest them while you type, in bahn.de's own order (up to 10). Returns each place's id, name, type (station, address or point of interest), station number, coordinates and the kinds of transport that stop there. Pass a place's id to bahn.de/search_journeys as origin or destination. A city name in capitals, such as MUNICH (MÜNCHEN), stands for all the stations of that city. Names are in English where bahn.de has an English name, with the local name in brackets. bahn.de's matching is loose: a text it does not know still brings up places whose names start like it, so check the names before you search.

### How do I automatically suggest Deutsche Bahn (bahn.de) stations and places on bahn.de?

Ask an AI agent connected to Reduck to run reduck/bahn.de/suggest_locations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bahn.de/suggest_locations

### Is there a bahn.de API to suggest Deutsche Bahn (bahn.de) stations and places?

You do not need one. "Suggest Deutsche Bahn (bahn.de) stations and places" drives the real bahn.de pages in a browser, so it works whether or not bahn.de offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns places.

### Do I need to be logged in to bahn.de?

No. It only uses pages of bahn.de that are reachable without signing in.

### Does it change anything on bahn.de, or only read data?

It only reads. It looks things up on bahn.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bahn.de/suggest_locations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bahn.de/suggest_locations

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/bahn.de/suggest_locations
