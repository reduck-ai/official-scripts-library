# Search one-way flights on Google Flights

Automatically search one-way flights on Google Flights on google.com. Search one-way flights on Google Flights between two airports or cities, given as IATA codes ("CDG", or "PAR" for all Paris airports), on one date: a fixed date, or a number of days after today for searches that run on a schedule. You can set the passengers, the cabin, the maximum number of stops, the tab (best or cheapest) and the price currency. Returns the date searched and every flight the page lists: local departure and arrival times, duration, stops, airlines, the total price for all passengers (null when Google shows none), whether Google ranks it as a top flight, whether it is a self-transfer on separate tickets, the layovers, and each leg with its flight number and aircraft. A search with no flights returns an empty list. An unknown code, a route Google does not sell, a date in the past or more than about 11 months ahead, and an unsupported currency fail with a message that names the problem. On a managed browser, set a country.

- Site: google.com
- Address: `reduck/google.com/search_flights`
- Updated: 2026-10-23 (v29)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/search_flights`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/search_flights
```

## Input

- `origin` (string, required): Departure airport or city, as an IATA code: an airport ("CDG") or a city with all its airports ("PAR").
- `destination` (string, required): Arrival airport or city, as an IATA code: an airport ("NRT") or a city with all its airports ("TYO").
- `date` (string, optional): Departure date, YYYY-MM-DD. From today to about 11 months ahead. Give date or daysAhead, not both.
- `sort` (string, optional): Google Flights' tab: best (price and convenience) or cheapest, which also lists self-transfer itineraries.
- `cabin` (string, optional)
- `adults` (integer, optional)
- `children` (integer, optional): Passengers aged 2 to 11.
- `currency` (string, optional): ISO 4217 code of the currency for the prices, such as EUR or USD.
- `maxStops` (integer | null, optional): 0 for nonstop flights only, 1 for one stop or fewer, 2 for two stops or fewer, null for any number of stops.
- `daysAhead` (integer, optional): Departure date as a number of days after today (UTC), for searches that run on a schedule. Give date or daysAhead, not both.
- `infantsOnLap` (integer, optional): Infants under 2 on an adult's lap.
- `infantsInSeat` (integer, optional): Infants under 2 with their own seat.

## Output

- `date` (string, required): The departure date searched.
- `flights` (array, required)
- `currency` (string, required)

## FAQ

### What does "Search one-way flights on Google Flights" do?

Search one-way flights on Google Flights between two airports or cities, given as IATA codes ("CDG", or "PAR" for all Paris airports), on one date: a fixed date, or a number of days after today for searches that run on a schedule. You can set the passengers, the cabin, the maximum number of stops, the tab (best or cheapest) and the price currency. Returns the date searched and every flight the page lists: local departure and arrival times, duration, stops, airlines, the total price for all passengers (null when Google shows none), whether Google ranks it as a top flight, whether it is a self-transfer on separate tickets, the layovers, and each leg with its flight number and aircraft. A search with no flights returns an empty list. An unknown code, a route Google does not sell, a date in the past or more than about 11 months ahead, and an unsupported currency fail with a message that names the problem. On a managed browser, set a country.

### How do I automatically search one-way flights on Google Flights on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/search_flights, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/search_flights

### Is there a google.com API to search one-way flights on Google Flights?

You do not need one. "Search one-way flights on Google Flights" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Required: origin, destination. Optional: date, sort, cabin, adults, children, currency, maxStops, daysAhead, infantsOnLap, infantsInSeat.

### What does it return?

It returns date, flights, currency.

### Do I need to be logged in to google.com?

No. It only uses pages of google.com that are reachable without signing in.

### Does it change anything on google.com, or only read data?

It only reads. It looks things up on google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/search_flights, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/search_flights

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/search_flights
