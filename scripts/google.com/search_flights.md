# Search flights on Google Flights

Automatically search flights on Google Flights on google.com. Search one-way or round-trip flights on Google Flights between two airports or cities, given as IATA codes ("CDG", or "PAR" for all Paris airports): a fixed date, or a number of days after today for searches that run on a schedule. You can set the passengers, the cabin, the maximum number of stops, the tab (best or cheapest) and the price currency. Returns the dates searched and every flight the page lists: local departure and arrival times, duration, stops, airlines, the total price for all passengers (null when Google shows none), whether Google ranks it as a top flight, whether it is a self-transfer on separate tickets, the layovers, and each leg with its flight number and aircraft. A round trip has two steps, as on the site. With a return date, the answer lists the outbound flights, each priced for the round trip with the cheapest return Google pairs with it. Then pass the legs of the outbound flight you choose as outboundLegs, with the same search: the answer lists the return flights, each with the final round-trip price. A search with no flights returns an empty list. An unknown code, a route Google does not sell, a date in the past or more than about 11 months ahead, a return date before the departure date, and an unsupported currency fail with a message that names the problem. On a managed browser, set a country.

- Site: google.com
- Address: `reduck/google.com/search_flights`
- Updated: 2026-11-08 (v32)
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
- `maxStops` (integer | null, optional): 0 for nonstop flights only, 1 for one stop or fewer, 2 for two stops or fewer, null for any number of stops. On a round trip it applies to both ways.
- `daysAhead` (integer, optional): Departure date as a number of days after today (UTC), for searches that run on a schedule. Give date or daysAhead, not both.
- `returnDate` (string, optional): Return date, YYYY-MM-DD, for a round trip. On or after the departure date. Leave out returnDate and returnDaysAhead for a one-way search.
- `infantsOnLap` (integer, optional): Infants under 2 on an adult's lap.
- `outboundLegs` (array, optional): On a round trip, the outbound flight to fly: the legs of one flight from the answer of the same search without outboundLegs, passed unchanged. The answer then lists the return flights, each with the final round-trip price.
- `infantsInSeat` (integer, optional): Infants under 2 with their own seat.
- `returnDaysAhead` (integer, optional): Return date as a number of days after today (UTC), for a round trip that runs on a schedule. Give returnDate or returnDaysAhead, not both.

## Output

- `date` (string, required): The departure date searched.
- `flights` (array, required): The flights the page lists, in its order. An outbound flight Google no longer sells gives an empty list of return flights.
- `currency` (string, required)
- `direction` (any, required): outbound: the flights listed go from origin to destination. return: they go back, for the outbound flight given in outboundLegs.
- `returnDate` (string | null, required): The return date searched. Null for a one-way search.

## FAQ

### What does "Search flights on Google Flights" do?

Search one-way or round-trip flights on Google Flights between two airports or cities, given as IATA codes ("CDG", or "PAR" for all Paris airports): a fixed date, or a number of days after today for searches that run on a schedule. You can set the passengers, the cabin, the maximum number of stops, the tab (best or cheapest) and the price currency. Returns the dates searched and every flight the page lists: local departure and arrival times, duration, stops, airlines, the total price for all passengers (null when Google shows none), whether Google ranks it as a top flight, whether it is a self-transfer on separate tickets, the layovers, and each leg with its flight number and aircraft. A round trip has two steps, as on the site. With a return date, the answer lists the outbound flights, each priced for the round trip with the cheapest return Google pairs with it. Then pass the legs of the outbound flight you choose as outboundLegs, with the same search: the answer lists the return flights, each with the final round-trip price. A search with no flights returns an empty list. An unknown code, a route Google does not sell, a date in the past or more than about 11 months ahead, a return date before the departure date, and an unsupported currency fail with a message that names the problem. On a managed browser, set a country.

### How do I automatically search flights on Google Flights on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/search_flights, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/search_flights

### Is there a google.com API to search flights on Google Flights?

You do not need one. "Search flights on Google Flights" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Required: origin, destination. Optional: date, sort, cabin, adults, children, currency, maxStops, daysAhead, returnDate, infantsOnLap, outboundLegs, infantsInSeat, returnDaysAhead.

### What does it return?

It returns date, flights, currency, direction, returnDate.

### Do I need to be logged in to google.com?

No. It only uses pages of google.com that are reachable without signing in.

### Does it change anything on google.com, or only read data?

It only reads. It looks things up on google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/search_flights, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/search_flights

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/search_flights
