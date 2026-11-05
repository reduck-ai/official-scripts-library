# Search Google Calendar events

Automatically search Google Calendar events on calendar.google.com. Search the signed-in Google Calendar across all its calendars, as the Calendar search box does. The query matches event content (title, description, location), not calendar names. Returns count, complete, timezone and events (id, calendar, eid, title, all_day, start, end, location), with start and end as wall-clock times in that timezone. Calendar returns 200 events at most, the nearest to today: complete is false when more matched, and there is no next page, so narrow the query or use list_events for a date range. Pass eid to get_event, update_event or delete_event.

- Site: calendar.google.com
- Address: `reduck/calendar.google.com/search_events`
- Updated: 2026-11-04 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendar.google.com/search_events`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/search_events
```

## Input

- `query` (string, required): Search text (same syntax as the Calendar search box)
- `account` (string, optional): The Google account to search, when this browser is signed in to several: its email, or its number in this browser ("1"), as mail.google.com/list_accounts lists them. The run fails if that account is not signed in. Omit for the first signed-in account.

## Output

- `count` (integer, required)
- `query` (string, required)
- `events` (array, required)
- `complete` (boolean, required): false when Calendar matched more events than it returns (200 at most, the nearest to today). Narrow the query, or use list_events for a date range.
- `account` (string | null, optional): Email of the Google account searched.
- `timezone` (string | null, optional): IANA timezone that start and end are in.

## FAQ

### What does "Search Google Calendar events" do?

Search the signed-in Google Calendar across all its calendars, as the Calendar search box does. The query matches event content (title, description, location), not calendar names. Returns count, complete, timezone and events (id, calendar, eid, title, all_day, start, end, location), with start and end as wall-clock times in that timezone. Calendar returns 200 events at most, the nearest to today: complete is false when more matched, and there is no next page, so narrow the query or use list_events for a date range. Pass eid to get_event, update_event or delete_event.

### How do I automatically search Google Calendar events on calendar.google.com?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/search_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/search_events

### Is there a calendar.google.com API to search Google Calendar events?

You do not need one. "Search Google Calendar events" drives the real calendar.google.com pages in a browser, so it works whether or not calendar.google.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: account.

### What does it return?

It returns count, query, events, account, complete, timezone.

### Do I need to be logged in to calendar.google.com?

Yes. It acts as you on calendar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendar.google.com cookies saved by the Reduck extension.

### Does it change anything on calendar.google.com, or only read data?

It only reads. It looks things up on calendar.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/search_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/search_events

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendar.google.com/search_events
