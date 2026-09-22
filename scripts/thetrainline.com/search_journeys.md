# Search train journeys (+ all stops)

Automatically search train journeys (+ all stops) on thetrainline.com. Search train journeys between two cities/stations on a date via Trainline: departure/arrival times, duration, changes, legs (train number, carrier). With includeStops=true, also returns every calling point of each train (all stops with scheduled times, platform, realtime status when available).

- Site: thetrainline.com
- Address: `reduck/thetrainline.com/search_journeys`
- Updated: 2026-08-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/thetrainline.com/search_journeys`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/thetrainline.com/search_journeys
```

## Input

- `to` (string, required): Destination city or station, free text
- `date` (string, required): Outbound date 'YYYY-MM-DD' (defaults to 08:00) or 'YYYY-MM-DDTHH:mm' — journeys departing after this time
- `from` (string, required): Origin city or station, free text (e.g. 'Paris', 'Lyon Part-Dieu', 'London')
- `max` (integer, optional): Max journeys returned (no pagination fan-out; the site returns ~8 per search). Default 10.
- `includeStops` (boolean, optional): If true, fetch all calling points (every stop of the full train route, incl. before/after the searched segment) for each leg. Default false.

## Output

- `origin` (object, required): Resolved origin (first autocomplete match)
- `journeys` (array, required)
- `destination` (object, required): Resolved destination

## FAQ

### What does "Search train journeys (+ all stops)" do?

Search train journeys between two cities/stations on a date via Trainline: departure/arrival times, duration, changes, legs (train number, carrier). With includeStops=true, also returns every calling point of each train (all stops with scheduled times, platform, realtime status when available).

### How do I automatically search train journeys (+ all stops) on thetrainline.com?

Ask an AI agent connected to Reduck to run reduck/thetrainline.com/search_journeys, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/thetrainline.com/search_journeys

### Is there a thetrainline.com API to search train journeys (+ all stops)?

You do not need one. "Search train journeys (+ all stops)" drives the real thetrainline.com pages in a browser, so it works whether or not thetrainline.com offers an API for this.

### What information do I need to provide?

Required: from, to, date. Optional: max, includeStops.

### What does it return?

It returns origin, journeys, destination.

### Do I need to be logged in to thetrainline.com?

No. It only uses pages of thetrainline.com that are reachable without signing in.

### Does it change anything on thetrainline.com, or only read data?

It only reads. It looks things up on thetrainline.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/thetrainline.com/search_journeys, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/thetrainline.com/search_journeys

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/thetrainline.com/search_journeys
