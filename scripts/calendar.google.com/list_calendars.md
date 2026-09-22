# List Google Calendars

Automatically list Google Calendars on calendar.google.com. List the signed-in Google Calendar account's calendars (primary + subscribed/secondary). Returns count and calendars (id, name, primary, timezone). The id is the join key you pass as calendarId to list_events/create_event to target a specific calendar; name for the primary calendar is the account's display name (Google leaves the primary's own name blank). Auto-generated helpers like Birthdays/Tasks are not returned.

- Site: calendar.google.com
- Address: `reduck/calendar.google.com/list_calendars`
- Updated: 2026-08-27 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendar.google.com/list_calendars`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/list_calendars
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `calendars` (array, required)

## FAQ

### What does "List Google Calendars" do?

List the signed-in Google Calendar account's calendars (primary + subscribed/secondary). Returns count and calendars (id, name, primary, timezone). The id is the join key you pass as calendarId to list_events/create_event to target a specific calendar; name for the primary calendar is the account's display name (Google leaves the primary's own name blank). Auto-generated helpers like Birthdays/Tasks are not returned.

### How do I automatically list Google Calendars on calendar.google.com?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/list_calendars, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/list_calendars

### Is there a calendar.google.com API to list Google Calendars?

You do not need one. "List Google Calendars" drives the real calendar.google.com pages in a browser, so it works whether or not calendar.google.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, calendars.

### Do I need to be logged in to calendar.google.com?

Yes. It acts as you on calendar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendar.google.com cookies saved by the Reduck extension.

### Does it change anything on calendar.google.com, or only read data?

It only reads. It looks things up on calendar.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/list_calendars, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/list_calendars

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendar.google.com/list_calendars
