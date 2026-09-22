# Search Events (FR)

Automatically search Events (FR) on ticketmaster.fr. Search Ticketmaster France for events by keyword. Returns each event's starting price in EUR, venue, city, genre, and date.

- Site: ticketmaster.fr
- Address: `reduck/ticketmaster.fr/search_events`
- Updated: 2026-09-21 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ticketmaster.fr/search_events`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ticketmaster.fr/search_events
```

## Input

- `query` (string, required): Search keyword — an artist, event name, or venue (e.g. "concert", "angele").
- `count` (integer, optional): How many results to return (page 1 of Ticketmaster's own relevance-ordered results).

## Output

- `query` (string, required)
- `total` (integer, required): Total matching events Ticketmaster France reports for this query.
- `artist` (object | null, required): The artist the query resolved to, when Ticketmaster answered with one artist rather than a result list. Null for an ordinary keyword search.
- `events` (array, required)
- `resolvedVia` (string, required): How Ticketmaster answered: "search" for a keyword result list, "artist" when the term named one artist and the events are that artist's, listed newest first rather than by relevance.

## FAQ

### What does "Search Events (FR)" do?

Search Ticketmaster France for events by keyword. Returns each event's starting price in EUR, venue, city, genre, and date.

### How do I automatically search Events (FR) on ticketmaster.fr?

Ask an AI agent connected to Reduck to run reduck/ticketmaster.fr/search_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ticketmaster.fr/search_events

### Is there a ticketmaster.fr API to search Events (FR)?

You do not need one. "Search Events (FR)" drives the real ticketmaster.fr pages in a browser, so it works whether or not ticketmaster.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: count.

### What does it return?

It returns query, total, artist, events, resolvedVia.

### Do I need to be logged in to ticketmaster.fr?

No. It only uses pages of ticketmaster.fr that are reachable without signing in.

### Does it change anything on ticketmaster.fr, or only read data?

It only reads. It looks things up on ticketmaster.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ticketmaster.fr/search_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ticketmaster.fr/search_events

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ticketmaster.fr/search_events
