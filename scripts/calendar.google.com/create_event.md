# Create a Google Calendar event

Automatically create a Google Calendar event on calendar.google.com. Create an event on the signed-in Google Calendar's primary calendar. Optionally invite guests (each gets an invitation email; external guests are auto-confirmed). Returns the new event's id, which you can pass to delete_event. A Google Meet link may be auto-added, depending on the account's default.

- Site: calendar.google.com
- Address: `reduck/calendar.google.com/create_event`
- Updated: 2026-09-03 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendar.google.com/create_event`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/create_event
```

## Input

- `end` (string, required): End: ISO datetime for timed, or YYYY-MM-DD (exclusive) for all_day
- `start` (string, required): Start: ISO datetime (2026-07-10T09:00:00) for timed, or YYYY-MM-DD for all_day
- `title` (string, required): Event title
- `guests` (array, optional): Guest email addresses to invite; an invitation email is sent to each (external guests auto-confirmed)
- `all_day` (boolean, optional)
- `location` (string, optional)
- `timezone` (string, optional): IANA timezone for timed events
- `description` (string, optional)

## Output

- `end` (string, required)
- `start` (string, required)
- `title` (string, required)
- `all_day` (boolean, required)
- `created` (boolean, required)
- `eid` (string | null, optional): Base64 event handle for delete_event; null if the post-save read-back missed it across all retries
- `guests` (array, optional)
- `html_link` (string | null, optional)

## FAQ

### What does "Create a Google Calendar event" do?

Create an event on the signed-in Google Calendar's primary calendar. Optionally invite guests (each gets an invitation email; external guests are auto-confirmed). Returns the new event's id, which you can pass to delete_event. A Google Meet link may be auto-added, depending on the account's default.

### How do I automatically create a Google Calendar event on calendar.google.com?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/create_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/create_event

### Is there a calendar.google.com API to create a Google Calendar event?

You do not need one. "Create a Google Calendar event" drives the real calendar.google.com pages in a browser, so it works whether or not calendar.google.com offers an API for this.

### What information do I need to provide?

Required: title, start, end. Optional: guests, all_day, location, timezone, description.

### What does it return?

It returns eid, end, start, title, guests, all_day, created, html_link.

### Do I need to be logged in to calendar.google.com?

Yes. It acts as you on calendar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendar.google.com cookies saved by the Reduck extension.

### Does it change anything on calendar.google.com, or only read data?

It makes changes on calendar.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/create_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/create_event

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendar.google.com/create_event
