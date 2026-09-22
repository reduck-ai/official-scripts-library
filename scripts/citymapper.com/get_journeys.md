# Get journeys (Citymapper)

Automatically get journeys (Citymapper) on citymapper.com. Public-transport journey options between two lat/lng points on citymapper.com, optionally for a given departure (departAt) or arrival (arriveBy) local time. Returns Citymapper's suggested journeys (duration, price, leave/arrive times, legs with mode and line) plus walk and cycle durations. No login needed. Works worldwide — Citymapper auto-detects the region from the coordinates; pass regionId only to force a specific one.

- Site: citymapper.com
- Address: `reduck/citymapper.com/get_journeys`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/citymapper.com/get_journeys`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/citymapper.com/get_journeys
```

## Input

- `end` (object, required)
- `start` (object, required)
- `arriveBy` (string, optional): Local arrival deadline, e.g. 2026-09-03T09:00.
- `departAt` (string, optional): Local departure time, e.g. 2026-09-03T09:00. Mutually exclusive with arriveBy; omit both for 'now'.
- `regionId` (string, optional): Optional Citymapper region id (e.g. fr-paris, uk-london). Citymapper auto-detects the region from the start/end coordinates when omitted, so this is only needed to force a specific region.

## Output

- `journeys` (array, required)
- `url` (string, optional)
- `timeMode` (string, optional)
- `walkMinutes` (integer | null, optional)
- `cycleMinutes` (integer | null, optional)
- `bestTransitMinutes` (integer | null, optional)

## FAQ

### What does "Get journeys (Citymapper)" do?

Public-transport journey options between two lat/lng points on citymapper.com, optionally for a given departure (departAt) or arrival (arriveBy) local time. Returns Citymapper's suggested journeys (duration, price, leave/arrive times, legs with mode and line) plus walk and cycle durations. No login needed. Works worldwide — Citymapper auto-detects the region from the coordinates; pass regionId only to force a specific one.

### How do I automatically get journeys (Citymapper) on citymapper.com?

Ask an AI agent connected to Reduck to run reduck/citymapper.com/get_journeys, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/citymapper.com/get_journeys

### Is there a citymapper.com API to get journeys (Citymapper)?

You do not need one. "Get journeys (Citymapper)" drives the real citymapper.com pages in a browser, so it works whether or not citymapper.com offers an API for this.

### What information do I need to provide?

Required: start, end. Optional: arriveBy, departAt, regionId.

### What does it return?

It returns url, journeys, timeMode, walkMinutes, cycleMinutes, bestTransitMinutes.

### Do I need to be logged in to citymapper.com?

No. It only uses pages of citymapper.com that are reachable without signing in.

### Does it change anything on citymapper.com, or only read data?

It only reads. It looks things up on citymapper.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/citymapper.com/get_journeys, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/citymapper.com/get_journeys

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/citymapper.com/get_journeys
