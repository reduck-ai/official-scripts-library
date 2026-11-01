# Suggest SNCF Connect places

Automatically suggest SNCF Connect places on sncf-connect.com. Look up places on SNCF Connect by name, as its Departure and Arrival fields suggest them while you type, in SNCF's own order: cities and stations, then city stops, points of interest and addresses. Returns each place's id, label, type, description (often its region or country) and the group SNCF lists it in. Pass a place unchanged to sncf-connect.com/search_journeys as origin or destination. A text SNCF has no suggestion for returns an empty list.

- Site: sncf-connect.com
- Address: `reduck/sncf-connect.com/suggest_places`
- Updated: 2026-10-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/sncf-connect.com/suggest_places`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/suggest_places
```

## Input

- `query` (string, required): A city, station or place name, as you would type it in SNCF Connect's Departure field, e.g. 'Munich' or 'Paris Gare de Lyon'.

## Output

- `places` (array, required): SNCF's suggestions, in its order. Empty when it has none.

## FAQ

### What does "Suggest SNCF Connect places" do?

Look up places on SNCF Connect by name, as its Departure and Arrival fields suggest them while you type, in SNCF's own order: cities and stations, then city stops, points of interest and addresses. Returns each place's id, label, type, description (often its region or country) and the group SNCF lists it in. Pass a place unchanged to sncf-connect.com/search_journeys as origin or destination. A text SNCF has no suggestion for returns an empty list.

### How do I automatically suggest SNCF Connect places on sncf-connect.com?

Ask an AI agent connected to Reduck to run reduck/sncf-connect.com/suggest_places, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/suggest_places

### Is there a sncf-connect.com API to suggest SNCF Connect places?

You do not need one. "Suggest SNCF Connect places" drives the real sncf-connect.com pages in a browser, so it works whether or not sncf-connect.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns places.

### Do I need to be logged in to sncf-connect.com?

No. It only uses pages of sncf-connect.com that are reachable without signing in.

### Does it change anything on sncf-connect.com, or only read data?

It only reads. It looks things up on sncf-connect.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/sncf-connect.com/suggest_places, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/suggest_places

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/sncf-connect.com/suggest_places
