# Search Google Calendar events

Automatically search Google Calendar events on calendar.google.com. Full-text search the signed-in Google Calendar across all its calendars, the same as the Calendar search box. Returns count and events (id, calendar, eid, title, all_day, start, end, location). start/end are the event's local wall-clock (ISO, no zone); eid is the base64 join key for delete_event. The query matches event content (title/description/location), not calendar names; supports whatever the Calendar search box supports.

- Site: calendar.google.com
- Address: `reduck/calendar.google.com/search_events`
- Updated: 2026-07-20 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendar.google.com/search_events`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/search_events
```

## Input

- `query` (string, required): Search text (same syntax as the Calendar search box)

## Output

- `count` (integer, required)
- `query` (string, required)
- `events` (array, required)

## FAQ

### What does "Search Google Calendar events" do?

Full-text search the signed-in Google Calendar across all its calendars, the same as the Calendar search box. Returns count and events (id, calendar, eid, title, all_day, start, end, location). start/end are the event's local wall-clock (ISO, no zone); eid is the base64 join key for delete_event. The query matches event content (title/description/location), not calendar names; supports whatever the Calendar search box supports.

### How do I automatically search Google Calendar events on calendar.google.com?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/search_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/search_events

### Is there a calendar.google.com API to search Google Calendar events?

You do not need one. "Search Google Calendar events" drives the real calendar.google.com pages in a browser, so it works whether or not calendar.google.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns count, query, events.

### Do I need to be logged in to calendar.google.com?

Yes. It acts as you on calendar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendar.google.com cookies saved by the Reduck extension.

### Does it change anything on calendar.google.com, or only read data?

Unknown: its author has not declared whether it changes anything on calendar.google.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/search_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/search_events

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendar.google.com/search_events
