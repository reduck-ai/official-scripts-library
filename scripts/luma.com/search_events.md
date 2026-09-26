# Luma API: search events by topic or city

Automatically search events by topic or city on luma.com. An unofficial Luma API: search public events by topic or city programmatically, from code or from an AI agent, with typed JSON in and out. Luma's official API is for hosts managing their own events and has no public event search.

- Site: luma.com
- Address: `reduck/luma.com/search_events`
- Updated: 2026-09-25 (v5)
- Author: Reduck AI (reduck)

## About

Developers looking for a Luma API to search public events by topic or city usually find there is none they can use: Luma's official API is for hosts managing their own events and has no public event search. This script fills that gap. It works like an API endpoint — one call with typed arguments, a JSON response — but runs through a real browser, yours or a hosted one, so it needs no Luma developer account, API key or app review.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/luma.com/search_events`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/luma.com/search_events
```

## Input

- `city` (string, optional): Curated Luma city slug to filter by (e.g. "paris", "london", "new-york"). Mutually exclusive with topic.
- `limit` (integer, optional): Max events to return per call. Default 25.
- `topic` (string, optional): Category slug to filter by (e.g. "crypto", "arts-culture", "fitness"). Mutually exclusive with city. Some categories are only served per-place and cannot be browsed globally; those fail naming the slug, and the way to browse them is `city`.
- `cursor` (string, optional): Pagination cursor from a previous call's next_cursor.
- `latitude` (number, optional): Optional latitude to bias/sort results by proximity. Only affects ordering — it does NOT satisfy a category that Luma serves per-place.
- `longitude` (number, optional): Optional longitude to bias/sort results by proximity. Only affects ordering — it does NOT satisfy a category that Luma serves per-place.

## Output

- `events` (array, required)
- `has_more` (boolean, required)
- `next_cursor` (string | null, optional)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "events": [
    {
      "city": "…",
      "name": "Example",
      "slug": "…",
      "end_at": "2026-01-15T09:30:00Z",
      "address": "…",
      "is_free": true,
      "event_id": "abc123",
      "start_at": "2026-01-15T09:30:00Z",
      "timezone": "…",
      "cover_url": "https://example.com/item/123",
      "guest_count": 3,
      "calendar_name": "…",
      "calendar_slug": "…",
      "location_type": "…",
      "show_guest_list": true,
      "require_approval": true,
      "registration_availability": "…"
    }
  ],
  "has_more": true,
  "next_cursor": "…"
}
```

## FAQ

### What does "Luma API: search events by topic or city" do?

Search upcoming public events on Luma, filtered by a category topic (e.g. "crypto", "fitness") or a curated city (e.g. "paris", "london"), paginated.

### How do I automatically search events by topic or city on luma.com?

Ask an AI agent connected to Reduck to run reduck/luma.com/search_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/search_events

### Is there a luma.com API to search events by topic or city?

You do not need one. "Luma API: search events by topic or city" drives the real luma.com pages in a browser, so it works whether or not luma.com offers an API for this.

### What information do I need to provide?

Optional: city, limit, topic, cursor, latitude, longitude.

### What does it return?

It returns events, has_more, next_cursor.

### Do I need to be logged in to luma.com?

No. It only uses pages of luma.com that are reachable without signing in.

### Does it change anything on luma.com, or only read data?

It only reads. It looks things up on luma.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/luma.com/search_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/search_events

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Is there a Luma API to search public events by topic or city?

Not an official one you can use for this: Luma's official API is for hosts managing their own events and has no public event search. This script works as an unofficial Luma API for it: typed input, JSON output, callable from an AI agent over MCP, from the CLI, or over REST.

### How do I search public events by topic or city programmatically?

Call this script with its arguments and read the JSON it returns. It drives Luma in a real browser session, so there is no API key to request and nothing to reverse-engineer yourself.

Source: https://reduck.ai/explore/scripts/reduck/luma.com/search_events
