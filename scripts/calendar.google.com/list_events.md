# List Google Calendar events

Automatically list Google Calendar events on calendar.google.com. List the signed-in Google Calendar account's events between two dates (across all visible calendars). Returns n and events (id, eid, title, all_day, start, end, timezone, location, description, calendar, organizer, attendees with response status, created, html_link). eid is the join key for delete_event. Date filtering is done on UTC boundaries; one call covers up to ~11 months from `from` (loop with a later `from` for more). Calendar events only — Google Tasks and reminders are not included.

- Site: calendar.google.com
- Address: `reduck/calendar.google.com/list_events`
- Updated: 2026-08-06 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendar.google.com/list_events`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/list_events
```

## Input

- `to` (string, required): End date (inclusive), YYYY-MM-DD
- `from` (string, required): Start date (inclusive), YYYY-MM-DD

## Output

- `n` (integer, required)
- `to` (string, required)
- `from` (string, required)
- `events` (array, required)
- `calendars` (array, optional): Calendar ids actually queried for this window. An empty `events` with a populated `calendars` really means an empty range.

## FAQ

### What does "List Google Calendar events" do?

List the signed-in Google Calendar account's events between two dates (across all visible calendars). Returns n and events (id, eid, title, all_day, start, end, timezone, location, description, calendar, organizer, attendees with response status, created, html_link). eid is the join key for delete_event. Date filtering is done on UTC boundaries; one call covers up to ~11 months from `from` (loop with a later `from` for more). Calendar events only — Google Tasks and reminders are not included.

### How do I automatically list Google Calendar events on calendar.google.com?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/list_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/list_events

### Is there a calendar.google.com API to list Google Calendar events?

You do not need one. "List Google Calendar events" drives the real calendar.google.com pages in a browser, so it works whether or not calendar.google.com offers an API for this.

### What information do I need to provide?

Required: from, to.

### What does it return?

It returns n, to, from, events, calendars.

### Do I need to be logged in to calendar.google.com?

Yes. It acts as you on calendar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendar.google.com cookies saved by the Reduck extension.

### Does it change anything on calendar.google.com, or only read data?

Unknown: its author has not declared whether it changes anything on calendar.google.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/list_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/list_events

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendar.google.com/list_events
