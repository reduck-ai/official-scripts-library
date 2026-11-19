# List Google Calendar events

Automatically list Google Calendar events on calendar.google.com. List the signed-in Google Calendar account's events between two dates, across every calendar shown in the sidebar, or one calendar with calendarId (from list_calendars). Each occurrence of a repeating event is its own row, with recurring_event_id set to its series. Returns n and events (id, eid, title, all_day, start, end, timezone, location, description, calendar, organizer, attendees with response status, created, html_link). Times are UTC; all-day events use dates, with an exclusive end. One call covers up to one year. Pass eid to get_event, update_event, delete_event, add_conference_link or respond_invitation. Google Tasks and birthdays are not included.

- Site: calendar.google.com
- Address: `reduck/calendar.google.com/list_events`
- Updated: 2026-11-18 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendar.google.com/list_events`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/list_events
```

## Input

- `to` (string, required): End date (inclusive), YYYY-MM-DD
- `from` (string, required): Start date (inclusive), YYYY-MM-DD
- `account` (string, optional): The Google account to read, when this browser is signed in to several: its email, or its number in this browser ("1"), as mail.google.com/list_accounts lists them. The run fails if that account is not signed in. Omit for the first signed-in account.
- `calendarId` (string, optional): List one calendar only, by its id from calendar.google.com/list_calendars. Omit to list every calendar shown in the Calendar sidebar.

## Output

- `n` (integer, required)
- `to` (string, required)
- `from` (string, required)
- `events` (array, required)
- `account` (string | null, optional): Email of the Google account read.
- `calendars` (array, optional): Calendar ids queried for this range.

## FAQ

### What does "List Google Calendar events" do?

List the signed-in Google Calendar account's events between two dates, across every calendar shown in the sidebar, or one calendar with calendarId (from list_calendars). Each occurrence of a repeating event is its own row, with recurring_event_id set to its series. Returns n and events (id, eid, title, all_day, start, end, timezone, location, description, calendar, organizer, attendees with response status, created, html_link). Times are UTC; all-day events use dates, with an exclusive end. One call covers up to one year. Pass eid to get_event, update_event, delete_event, add_conference_link or respond_invitation. Google Tasks and birthdays are not included.

### How do I automatically list Google Calendar events on calendar.google.com?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/list_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/list_events

### Is there a calendar.google.com API to list Google Calendar events?

You do not need one. "List Google Calendar events" drives the real calendar.google.com pages in a browser, so it works whether or not calendar.google.com offers an API for this.

### What information do I need to provide?

Required: from, to. Optional: account, calendarId.

### What does it return?

It returns n, to, from, events, account, calendars.

### Do I need to be logged in to calendar.google.com?

Yes. It acts as you on calendar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendar.google.com cookies saved by the Reduck extension.

### Does it change anything on calendar.google.com, or only read data?

It only reads. It looks things up on calendar.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/list_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/list_events

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendar.google.com/list_events
