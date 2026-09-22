# SNCF Connect API: search train journeys and fares

Automatically search train journeys and fares on sncf-connect.com. An unofficial SNCF Connect API for train search: SNCF Connect has no public API for journeys and fares, and this returns them as JSON, programmatically. Search trains between two cities or stations on a given date via SNCF Connect. Returns each journey (times, duration, operator, best price) with all of its fare offers (class, fare name, price, flexibility, full conditions) and whether the fare can be cancelled free of charge. No journeys means no tickets are on sale for that date. Runs only via the local browser extension, not the hosted cloud browser.

- Site: sncf-connect.com
- Address: `reduck/sncf-connect.com/search_journeys`
- Updated: 2026-09-19 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/sncf-connect.com/search_journeys`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/search_journeys
```

## Input

- `date` (string, required): Outward date YYYY-MM-DD
- `origin` (string, required): Departure city or station, e.g. 'Turin' or 'Paris Gare de Lyon'
- `destination` (string, required): Arrival city or station, e.g. 'Paris'

## Output

- `date` (string, required)
- `origin` (string, required)
- `journeys` (array, required)
- `destination` (string, required)

## FAQ

### What does "SNCF Connect API: search train journeys and fares" do?

An unofficial SNCF Connect API for train search: SNCF Connect has no public API for journeys and fares, and this returns them as JSON, programmatically. Search trains between two cities or stations on a given date via SNCF Connect. Returns each journey (times, duration, operator, best price) with all of its fare offers (class, fare name, price, flexibility, full conditions) and whether the fare can be cancelled free of charge. No journeys means no tickets are on sale for that date. Runs only via the local browser extension, not the hosted cloud browser.

### How do I automatically search train journeys and fares on sncf-connect.com?

Ask an AI agent connected to Reduck to run reduck/sncf-connect.com/search_journeys, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/search_journeys

### Is there a sncf-connect.com API to search train journeys and fares?

You do not need one. "SNCF Connect API: search train journeys and fares" drives the real sncf-connect.com pages in a browser, so it works whether or not sncf-connect.com offers an API for this.

### What information do I need to provide?

Required: origin, destination, date.

### What does it return?

It returns date, origin, journeys, destination.

### Do I need to be logged in to sncf-connect.com?

No. It only uses pages of sncf-connect.com that are reachable without signing in.

### Does it change anything on sncf-connect.com, or only read data?

It only reads. It looks things up on sncf-connect.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/sncf-connect.com/search_journeys, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/search_journeys

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/sncf-connect.com/search_journeys
