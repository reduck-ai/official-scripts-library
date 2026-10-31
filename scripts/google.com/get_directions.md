# Get Google Maps directions

Automatically get Google Maps directions on google.com. Get the routes Google Maps proposes between two places by car, public transport, on foot or by bike, as its directions panel lists them. Places are addresses, place names or "lat,lng" coordinates, such as the coordinates that search_places or get_place return for a place, or that a listing search returns for a home. Public transport takes a time (leave now, depart at, arrive by, or the last departure of a day), preferred vehicles (bus, subway, train, tram) and a routing preference (fewer transfers, less walking, wheelchair accessible); driving takes the time and the roads to avoid (highways, tolls, ferries). Each route gives its duration, distance, departure and arrival times, fare, walking time and service frequency, and each of its legs: for public transport the line, vehicle, color, direction, operator, the boarding and alighting stops with platforms and times, and the stops in between; for driving the duration in traffic and the usual range. The answer also gives the place Maps resolved for each end, with its place id for get_place, which can differ from what was meant when the text is vague, and the duration Maps shows for each travel mode. When Maps finds no route, routes is empty. To compare many origins with one destination, run it once per origin in a single call with several scripts.

- Site: google.com
- Address: `reduck/google.com/get_directions`
- Updated: 2026-10-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/get_directions`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/get_directions
```

## Input

- `mode` (string, required): How to travel. transit is public transport.
- `origin` (string, required): Where the trip starts: an address, a place name with its city (e.g. 'Marienplatz, München'), or coordinates as 'lat,lng' (e.g. '48.1371,11.5754'). Coordinates are the most exact.
- `destination` (string, required): Where the trip ends, in the same forms as origin.
- `gl` (string, optional): Region, e.g. 'de'. Empty: the browser's region.
- `hl` (string, optional): Language of the texts Maps writes (vehicle names, instructions, fares), e.g. 'en'. Empty: the browser's language.
- `date` (string, optional): Day of the trip, YYYY-MM-DD, for depart_at, arrive_by and last_available. Default: today. Do not pass with daysFromToday.
- `time` (string, optional): Local time at the trip, HH:MM (24 h), for depart_at and arrive_by.
- `timeMode` (string, optional): transit and driving only. depart_at and arrive_by take time and a day; last_available (transit only) finds the last departures of the day.
- `avoidTolls` (boolean, optional): driving only.
- `avoidFerries` (boolean, optional): driving only.
- `includeStops` (boolean, optional): transit: also return the stops each vehicle passes between boarding and alighting (intermediateStops). Off by default to keep the answer short.
- `transitRoute` (string, optional): transit only: how Maps ranks the routes.
- `avoidHighways` (boolean, optional): driving only.
- `daysFromToday` (integer, optional): Day of the trip as a number of days after today (0 is today), for searches that run on a schedule. Do not pass with date.
- `transitVehicles` (array, optional): transit only: the vehicles to prefer (Maps' Prefer options; tram includes light rail). Empty: no preference.

## Output

- `mode` (string, required)
- `origin` (any, required): The place Maps resolved for the origin text.
- `routes` (array, required)
- `destination` (any, required)
- `durationsByMode` (object, optional): Seconds Maps shows on each travel mode tab for this trip; a mode Maps does not offer is absent.

## FAQ

### What does "Get Google Maps directions" do?

Get the routes Google Maps proposes between two places by car, public transport, on foot or by bike, as its directions panel lists them. Places are addresses, place names or "lat,lng" coordinates, such as the coordinates that search_places or get_place return for a place, or that a listing search returns for a home. Public transport takes a time (leave now, depart at, arrive by, or the last departure of a day), preferred vehicles (bus, subway, train, tram) and a routing preference (fewer transfers, less walking, wheelchair accessible); driving takes the time and the roads to avoid (highways, tolls, ferries). Each route gives its duration, distance, departure and arrival times, fare, walking time and service frequency, and each of its legs: for public transport the line, vehicle, color, direction, operator, the boarding and alighting stops with platforms and times, and the stops in between; for driving the duration in traffic and the usual range. The answer also gives the place Maps resolved for each end, with its place id for get_place, which can differ from what was meant when the text is vague, and the duration Maps shows for each travel mode. When Maps finds no route, routes is empty. To compare many origins with one destination, run it once per origin in a single call with several scripts.

### How do I automatically get Google Maps directions on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/get_directions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/get_directions

### Is there a google.com API to get Google Maps directions?

You do not need one. "Get Google Maps directions" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Required: origin, destination, mode. Optional: gl, hl, date, time, timeMode, avoidTolls, avoidFerries, includeStops, transitRoute, avoidHighways, daysFromToday, transitVehicles.

### What does it return?

It returns mode, origin, routes, destination, durationsByMode.

### Do I need to be logged in to google.com?

No. It only uses pages of google.com that are reachable without signing in.

### Does it change anything on google.com, or only read data?

It only reads. It looks things up on google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/get_directions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/get_directions

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/get_directions
