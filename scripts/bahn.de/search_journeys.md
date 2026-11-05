# Search Deutsche Bahn (bahn.de) train journeys and prices

Automatically search Deutsche Bahn (bahn.de) train journeys and prices on bahn.de. Search train journeys on Deutsche Bahn (bahn.de) between two places from bahn.de/suggest_locations, departing or arriving at a time on a date (or a number of days after today, for searches that run on a schedule), with the options bahn.de offers: class, travellers with their ages and discount cards (BahnCard and others), fastest connections, direct services only, transport modes, bicycle transport, seat booking only, Deutschland-Ticket. Returns the journeys bahn.de lists from that time (about 5 to 10), each with its planned and estimated times, duration, changes, the cheapest price bahn.de shows for the travellers asked (null when no ticket is on sale, and marked when the price covers only part of the journey), the expected occupancy per class, bahn.de's messages, and each leg (stations, platforms, train, operator, and, with includeStops, every stop). Pass laterCursor or earlierCursor back as cursor, with the same search, for the next or previous journeys. A route bahn.de has no connection on returns an empty list. bahn.de refuses searches for a few minutes after many in a short time: the run then fails and says so.

- Site: bahn.de
- Address: `reduck/bahn.de/search_journeys`
- Updated: 2026-11-04 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bahn.de/search_journeys`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bahn.de/search_journeys
```

## Input

- `origin` (string, required): The departure place: a place's id from bahn.de/suggest_locations, unchanged.
- `destination` (string, required): The arrival place: a place's id from bahn.de/suggest_locations, unchanged.
- `date` (string, optional): The travel date, YYYY-MM-DD. Give date or daysAhead, not both.
- `time` (string, optional): HH:mm, local time of the place: journeys departing from this time, or arriving by it with timeIs 'arrival'.
- `class` (integer, optional): Travel class the prices are for.
- `modes` (array, optional): The transport modes to use: ICE, EC_IC (Eurocity and Intercity), IR (Interregio), REGIONAL, SBAHN, BUS, SCHIFF (boat), UBAHN, TRAM, ANRUFPFLICHTIG (on-demand). All by default.
- `cursor` (string, optional): laterCursor or earlierCursor of an earlier answer to the same search: returns the next or previous journeys.
- `timeIs` (string, optional): Whether time is the departure time or the arrival time.
- `bicycle` (boolean, optional): Only journeys on which a bicycle can travel.
- `fastest` (boolean, optional): Show fastest connections only, as bahn.de does by default. False also lists slower connections that may be cheaper.
- `seatOnly` (boolean, optional): Book seat only: prices are for a seat reservation, for travellers who already hold a ticket.
- `daysAhead` (integer, optional): The travel date as a number of days after today (UTC), for searches that run on a schedule. Give date or daysAhead, not both.
- `directOnly` (boolean, optional): Direct services only: journeys with no change.
- `travellers` (array, optional): Who travels, as groups of one kind. bahn.de prices the journey for all of them.
- `viableOnly` (boolean, optional): Viable connections only: leave out the journeys bahn.de expects to miss a change, for delays or cancellations.
- `includeStops` (boolean, optional): Also return every stop of each leg, with its times and platform.
- `hasDeutschlandTicket` (boolean, optional): The travellers hold a Deutschland-Ticket: bahn.de prices only the parts it does not cover.
- `deutschlandTicketOnly` (boolean, optional): Only journeys that the Deutschland-Ticket is valid for.

## Output

- `journeys` (array, required): The journeys bahn.de lists, in its order. Empty when it has no connection.
- `laterCursor` (string | null, required): Pass back as cursor, with the same search, for the journeys after these.
- `earlierCursor` (string | null, required): Pass back as cursor, with the same search, for the journeys before these.

## FAQ

### What does "Search Deutsche Bahn (bahn.de) train journeys and prices" do?

Search train journeys on Deutsche Bahn (bahn.de) between two places from bahn.de/suggest_locations, departing or arriving at a time on a date (or a number of days after today, for searches that run on a schedule), with the options bahn.de offers: class, travellers with their ages and discount cards (BahnCard and others), fastest connections, direct services only, transport modes, bicycle transport, seat booking only, Deutschland-Ticket. Returns the journeys bahn.de lists from that time (about 5 to 10), each with its planned and estimated times, duration, changes, the cheapest price bahn.de shows for the travellers asked (null when no ticket is on sale, and marked when the price covers only part of the journey), the expected occupancy per class, bahn.de's messages, and each leg (stations, platforms, train, operator, and, with includeStops, every stop). Pass laterCursor or earlierCursor back as cursor, with the same search, for the next or previous journeys. A route bahn.de has no connection on returns an empty list. bahn.de refuses searches for a few minutes after many in a short time: the run then fails and says so.

### How do I automatically search Deutsche Bahn (bahn.de) train journeys and prices on bahn.de?

Ask an AI agent connected to Reduck to run reduck/bahn.de/search_journeys, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bahn.de/search_journeys

### Is there a bahn.de API to search Deutsche Bahn (bahn.de) train journeys and prices?

You do not need one. "Search Deutsche Bahn (bahn.de) train journeys and prices" drives the real bahn.de pages in a browser, so it works whether or not bahn.de offers an API for this.

### What information do I need to provide?

Required: origin, destination. Optional: date, time, class, modes, cursor, timeIs, bicycle, fastest, seatOnly, daysAhead, directOnly, travellers, viableOnly, includeStops, hasDeutschlandTicket, deutschlandTicketOnly.

### What does it return?

It returns journeys, laterCursor, earlierCursor.

### Do I need to be logged in to bahn.de?

No. It only uses pages of bahn.de that are reachable without signing in.

### Does it change anything on bahn.de, or only read data?

It only reads. It looks things up on bahn.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bahn.de/search_journeys, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bahn.de/search_journeys

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/bahn.de/search_journeys
