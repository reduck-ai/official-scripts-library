# Search Eventbrite events

Automatically search Eventbrite events on eventbrite.com. Search Eventbrite for events by keyword in a city, or online, one results page at a time. Returns each event's id, name, link, dates and times, time zone, venue and address, whether it is online, its summary, organizer id, categories and image, plus the total number of matching events and pages.

- Site: eventbrite.com
- Address: `reduck/eventbrite.com/search_events`
- Updated: 2026-10-02 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/eventbrite.com/search_events`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/eventbrite.com/search_events
```

## Input

- `query` (string, required): What to search for, e.g. "ai", "startup networking", "jazz".
- `location` (string, required): Where: "City, Country" (e.g. "Paris, France", "Austin, United States"), an Eventbrite place slug as it appears in its URLs (e.g. "france--paris", "ca--san-francisco"), or "online" for online events.
- `page` (integer, optional): Results page, 1-based. The response says how many pages exist.

## Output

- `page` (integer, required)
- `query` (string, required)
- `total` (integer | null, required): Event count Eventbrite reports for the search. It reflects the place more than the keyword, so it can be much larger than the number of closely matching events.
- `events` (array, required)
- `location` (string, required): The place Eventbrite searched, as its own slug (it may correct or broaden the one given).
- `pageCount` (integer | null, required): Number of result pages Eventbrite reports for this search.

## FAQ

### What does "Search Eventbrite events" do?

Search Eventbrite for events by keyword in a city, or online, one results page at a time. Returns each event's id, name, link, dates and times, time zone, venue and address, whether it is online, its summary, organizer id, categories and image, plus the total number of matching events and pages.

### How do I automatically search Eventbrite events on eventbrite.com?

Ask an AI agent connected to Reduck to run reduck/eventbrite.com/search_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/eventbrite.com/search_events

### Is there a eventbrite.com API to search Eventbrite events?

You do not need one. "Search Eventbrite events" drives the real eventbrite.com pages in a browser, so it works whether or not eventbrite.com offers an API for this.

### What information do I need to provide?

Required: query, location. Optional: page.

### What does it return?

It returns page, query, total, events, location, pageCount.

### Do I need to be logged in to eventbrite.com?

No. It only uses pages of eventbrite.com that are reachable without signing in.

### Does it change anything on eventbrite.com, or only read data?

It only reads. It looks things up on eventbrite.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/eventbrite.com/search_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/eventbrite.com/search_events

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/eventbrite.com/search_events
