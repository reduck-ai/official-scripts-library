# Get Google Calendar event

Automatically get Google Calendar event on calendar.google.com. Read one Google Calendar event by its eid: title, all_day, timezone, start, end, location, description, guests (email addresses) and Meet link. Start and end are wall-clock ISO times in the event's own timezone, or dates for an all-day event. Pass account to read as one of several signed-in Google accounts. An eid this account cannot open is an error that says so.

- Site: calendar.google.com
- Address: `reduck/calendar.google.com/get_event`
- Updated: 2026-11-06 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendar.google.com/get_event`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/get_event
```

## Input

- `eid` (string, optional): The event's eid, from list_events, search_events or create_event.
- `account` (string, optional): The Google account to read as, when this browser is signed in to several: its email, or its number in this browser ("1"), as mail.google.com/list_accounts lists them. The run fails if that account is not signed in. Omit for the first signed-in account.
- `eventid` (string, optional): Same as eid. Kept for callers that use this name.

## Output

- `eid` (string, required)
- `guests` (array, required)
- `end` (string | null, optional): Wall-clock ISO in `timezone` (no offset), or YYYY-MM-DD for all day (inclusive, as Calendar shows it).
- `start` (string | null, optional): Wall-clock ISO in `timezone` (no offset), or YYYY-MM-DD for all day.
- `title` (string | null, optional)
- `account` (string | null, optional): Email of the Google account read as.
- `all_day` (boolean | null, optional)
- `eventid` (string, optional)
- `location` (string | null, optional)
- `meetLink` (string | null, optional)
- `timezone` (string | null, optional): IANA timezone that start and end are in (null for all day).
- `description` (string | null, optional)

## FAQ

### What does "Get Google Calendar event" do?

Read one Google Calendar event by its eid: title, all_day, timezone, start, end, location, description, guests (email addresses) and Meet link. Start and end are wall-clock ISO times in the event's own timezone, or dates for an all-day event. Pass account to read as one of several signed-in Google accounts. An eid this account cannot open is an error that says so.

### How do I automatically get Google Calendar event on calendar.google.com?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/get_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/get_event

### Is there a calendar.google.com API to get Google Calendar event?

You do not need one. "Get Google Calendar event" drives the real calendar.google.com pages in a browser, so it works whether or not calendar.google.com offers an API for this.

### What information do I need to provide?

Optional: eid, account, eventid.

### What does it return?

It returns eid, end, start, title, guests, account, all_day, eventid, location, meetLink, timezone, description.

### Do I need to be logged in to calendar.google.com?

Yes. It acts as you on calendar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendar.google.com cookies saved by the Reduck extension.

### Does it change anything on calendar.google.com, or only read data?

It only reads. It looks things up on calendar.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/get_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/get_event

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendar.google.com/get_event
