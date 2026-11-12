# SNCF Connect unofficial API: search train journeys and fares

Automatically search train journeys and fares on sncf-connect.com. An unofficial SNCF Connect API for train search: SNCF Connect has no public API for journeys and fares, and this returns them as JSON, programmatically. Search trains between two places on a date or a number of days after today (for searches that run on a schedule), from a time of day, Paris time. Give each place as sncf-connect.com/suggest_places returns it, or by its name: a name is used only when SNCF has exactly one city (else one place) with that exact label, and otherwise fails with the candidates. Returns SNCF's status for the search and each journey it lists from about that time (a page of about 5 to 10): times, duration, operator, best price, and all of its fare offers (class, fare name, price, flexibility label, and the exchange and refund conditions as SNCF writes them). A train not yet on sale has no offers. For later trains, search again from a later time. No journeys, with a status other than RESULTS, means no tickets are on sale for that date. International routes are on sale for a shorter time ahead than domestic ones.

- Site: sncf-connect.com
- Address: `reduck/sncf-connect.com/search_journeys`
- Updated: 2026-11-11 (v21)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/sncf-connect.com/search_journeys`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/search_journeys
```

## Input

- `origin` (any, required): The departure place: a place from sncf-connect.com/suggest_places ({ id, label }), passed unchanged, or a name, used only when SNCF has exactly one city (else one place) with that exact label.
- `destination` (any, required): The arrival place: a place from sncf-connect.com/suggest_places ({ id, label }), passed unchanged, or a name, used only when SNCF has exactly one city (else one place) with that exact label.
- `date` (string, optional): Outward date, YYYY-MM-DD. Give date or daysAhead, not both.
- `time` (string, optional): Search from this time, HH:mm, Paris time. For later trains, search again from a later time.
- `daysAhead` (integer, optional): Outward date as a number of days after today (UTC), for searches that run on a schedule. Give date or daysAhead, not both.

## Output

- `date` (string, required): The outward date searched.
- `time` (string, required): The time searched from, Paris time.
- `status` (string | null, required): SNCF's status for the search, e.g. RESULTS. Another value says why there are no journeys.
- `journeys` (array, required): The journeys SNCF lists from about the time searched, in its order (a page of about 5 to 10). Empty when no tickets are on sale for that date.

## FAQ

### What does "SNCF Connect unofficial API: search train journeys and fares" do?

An unofficial SNCF Connect API for train search: SNCF Connect has no public API for journeys and fares, and this returns them as JSON, programmatically. Search trains between two places on a date or a number of days after today (for searches that run on a schedule), from a time of day, Paris time. Give each place as sncf-connect.com/suggest_places returns it, or by its name: a name is used only when SNCF has exactly one city (else one place) with that exact label, and otherwise fails with the candidates. Returns SNCF's status for the search and each journey it lists from about that time (a page of about 5 to 10): times, duration, operator, best price, and all of its fare offers (class, fare name, price, flexibility label, and the exchange and refund conditions as SNCF writes them). A train not yet on sale has no offers. For later trains, search again from a later time. No journeys, with a status other than RESULTS, means no tickets are on sale for that date. International routes are on sale for a shorter time ahead than domestic ones.

### How do I automatically search train journeys and fares on sncf-connect.com?

Ask an AI agent connected to Reduck to run reduck/sncf-connect.com/search_journeys, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/search_journeys

### Is there a sncf-connect.com API to search train journeys and fares?

You do not need one. "SNCF Connect unofficial API: search train journeys and fares" drives the real sncf-connect.com pages in a browser, so it works whether or not sncf-connect.com offers an API for this.

### What information do I need to provide?

Required: origin, destination. Optional: date, time, daysAhead.

### What does it return?

It returns date, time, status, journeys.

### Do I need to be logged in to sncf-connect.com?

No. It only uses pages of sncf-connect.com that are reachable without signing in.

### Does it change anything on sncf-connect.com, or only read data?

It only reads. It looks things up on sncf-connect.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/sncf-connect.com/search_journeys, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/search_journeys

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/sncf-connect.com/search_journeys
