# Search Events

Automatically search Events on ticketmaster.com. Search Ticketmaster for events by keyword and return the top results (title, id, url, venue/city/state, start date, cancelled/soldOut flags) read from the search page's own hydration state.

- Site: ticketmaster.com
- Address: `reduck/ticketmaster.com/search_events`
- Updated: 2026-09-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ticketmaster.com/search_events`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ticketmaster.com/search_events
```

## Input

- `query` (string, required): Search keyword, e.g. "concert", an artist name, or a venue.
- `count` (integer, optional): How many top results to return (page 1 of Ticketmaster's own results, which renders up to 20).

## Output

- `query` (string, required)
- `total` (integer, required): Total result count Ticketmaster reports for this query.
- `events` (array, required)

## FAQ

### What does "Search Events" do?

Search Ticketmaster for events by keyword and return the top results (title, id, url, venue/city/state, start date, cancelled/soldOut flags) read from the search page's own hydration state.

### How do I automatically search Events on ticketmaster.com?

Ask an AI agent connected to Reduck to run reduck/ticketmaster.com/search_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ticketmaster.com/search_events

### Is there a ticketmaster.com API to search Events?

You do not need one. "Search Events" drives the real ticketmaster.com pages in a browser, so it works whether or not ticketmaster.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: count.

### What does it return?

It returns query, total, events.

### Do I need to be logged in to ticketmaster.com?

Yes. It acts as you on ticketmaster.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the ticketmaster.com cookies saved by the Reduck extension.

### Does it change anything on ticketmaster.com, or only read data?

It only reads. It looks things up on ticketmaster.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ticketmaster.com/search_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ticketmaster.com/search_events

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ticketmaster.com/search_events
