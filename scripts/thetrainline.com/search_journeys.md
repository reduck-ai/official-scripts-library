# Search Trainline train journeys (+ all stops)

Automatically search Trainline train journeys (+ all stops) on thetrainline.com. Search train journeys on Trainline between two stations or cities, given as Trainline codes from thetrainline.com/suggest_locations, on a date or a number of days after today (for searches that run on a schedule), from a time of day. Returns the journeys Trainline lists from about that time (about 10), across carriers such as SNCF and Deutsche Bahn: departure and arrival times, ISO duration, changes and legs (stations, train, train number, carrier), and the prices as Trainline sells them. A journey is sold as one ticket or as several, and each ticket lists its offers: price, currency, flexibility, seller, and each fare's name, exchange and refund conditions and class on each train. For later trains, search again from a later time. With includeStops=true, each leg also gets every calling point of its train with scheduled times, platform and live status; Trainline has these only for near-term trains, so a leg far ahead gets null. A route Trainline sells no tickets on returns an empty list.

- Site: thetrainline.com
- Address: `reduck/thetrainline.com/search_journeys`
- Updated: 2026-10-31 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/thetrainline.com/search_journeys`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/thetrainline.com/search_journeys
```

## Input

- `origin` (string, required): Trainline code of the departure station or city, from thetrainline.com/suggest_locations (e.g. urn:trainline:generic:loc:4916 for Paris).
- `destination` (string, required): Trainline code of the arrival station or city, from thetrainline.com/suggest_locations.
- `date` (string, optional): Outward date, YYYY-MM-DD. Give date or daysAhead, not both.
- `time` (string, optional): Journeys departing after this time, HH:mm, local time. For later trains, search again from a later time.
- `daysAhead` (integer, optional): Outward date as a number of days after today (UTC), for searches that run on a schedule. Give date or daysAhead, not both.
- `includeStops` (boolean, optional): If true, also return all calling points (every stop of the full train route, incl. before/after the searched segment) for each leg.

## Output

- `journeys` (array, required): The journeys Trainline lists from the time asked (about 10), in its order. Empty when it sells no tickets on the route.

## FAQ

### What does "Search Trainline train journeys (+ all stops)" do?

Search train journeys on Trainline between two stations or cities, given as Trainline codes from thetrainline.com/suggest_locations, on a date or a number of days after today (for searches that run on a schedule), from a time of day. Returns the journeys Trainline lists from about that time (about 10), across carriers such as SNCF and Deutsche Bahn: departure and arrival times, ISO duration, changes and legs (stations, train, train number, carrier), and the prices as Trainline sells them. A journey is sold as one ticket or as several, and each ticket lists its offers: price, currency, flexibility, seller, and each fare's name, exchange and refund conditions and class on each train. For later trains, search again from a later time. With includeStops=true, each leg also gets every calling point of its train with scheduled times, platform and live status; Trainline has these only for near-term trains, so a leg far ahead gets null. A route Trainline sells no tickets on returns an empty list.

### How do I automatically search Trainline train journeys (+ all stops) on thetrainline.com?

Ask an AI agent connected to Reduck to run reduck/thetrainline.com/search_journeys, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/thetrainline.com/search_journeys

### Is there a thetrainline.com API to search Trainline train journeys (+ all stops)?

You do not need one. "Search Trainline train journeys (+ all stops)" drives the real thetrainline.com pages in a browser, so it works whether or not thetrainline.com offers an API for this.

### What information do I need to provide?

Required: origin, destination. Optional: date, time, daysAhead, includeStops.

### What does it return?

It returns journeys.

### Do I need to be logged in to thetrainline.com?

No. It only uses pages of thetrainline.com that are reachable without signing in.

### Does it change anything on thetrainline.com, or only read data?

It only reads. It looks things up on thetrainline.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/thetrainline.com/search_journeys, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/thetrainline.com/search_journeys

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/thetrainline.com/search_journeys
