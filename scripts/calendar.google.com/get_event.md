# Get Google Calendar event

Automatically get Google Calendar event on calendar.google.com. Read a Google Calendar event's details by its opaque eventid (as returned by list_events): title, start, end, location, guests (deduped email addresses) and meetLink. Start and end are returned as the date/time strings Calendar displays, not as ISO timestamps.

- Site: calendar.google.com
- Address: `reduck/calendar.google.com/get_event`
- Updated: 2026-08-27 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendar.google.com/get_event`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/get_event
```

## Input

- `eventid` (string, required): Opaque event id (the eid field from list_events, NOT its id field — passing the raw id makes the edit page serve an HTTP 500).
- `account` (string, optional)

## Output

- `guests` (array, required)
- `eventid` (string, required)
- `end` (string | null, optional)
- `start` (string | null, optional)
- `title` (string | null, optional)
- `location` (string | null, optional)
- `meetLink` (string | null, optional)

## FAQ

### What does "Get Google Calendar event" do?

Read a Google Calendar event's details by its opaque eventid (as returned by list_events): title, start, end, location, guests (deduped email addresses) and meetLink. Start and end are returned as the date/time strings Calendar displays, not as ISO timestamps.

### How do I automatically get Google Calendar event on calendar.google.com?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/get_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/get_event

### Is there a calendar.google.com API to get Google Calendar event?

You do not need one. "Get Google Calendar event" drives the real calendar.google.com pages in a browser, so it works whether or not calendar.google.com offers an API for this.

### What information do I need to provide?

Required: eventid. Optional: account.

### What does it return?

It returns end, start, title, guests, eventid, location, meetLink.

### Do I need to be logged in to calendar.google.com?

Yes. It acts as you on calendar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendar.google.com cookies saved by the Reduck extension.

### Does it change anything on calendar.google.com, or only read data?

It only reads. It looks things up on calendar.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/get_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/get_event

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendar.google.com/get_event
