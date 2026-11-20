# Update a Google Calendar event

Automatically update a Google Calendar event on calendar.google.com. Edit an existing Google Calendar event by its eid (from list_events/search_events/create_event). Opens the event composer and applies only the fields you pass — title, start, end (ISO datetime, or YYYY-MM-DD with all_day), all_day, location, description, add_guests — then Saves, sending update/invitation emails to guests when present. Single (non-recurring) events; a recurring instance's this/all scope dialog isn't handled. Changing start alone shifts the end to keep the duration unless you also pass end.

- Site: calendar.google.com
- Address: `reduck/calendar.google.com/update_event`
- Updated: 2026-11-19 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendar.google.com/update_event`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/update_event
```

## Input

- `eid` (string, required): Event handle from list_events, search_events or create_event
- `end` (string, optional): New end: ISO datetime, or YYYY-MM-DD (exclusive) when all_day
- `start` (string, optional): New start: ISO datetime, or YYYY-MM-DD when all_day
- `title` (string, optional)
- `account` (string, optional): The Google account to edit as, when this browser is signed in to several: its email, or its number in this browser ("1"), as mail.google.com/list_accounts lists them. Use the account the eid came from. The run fails, changing nothing, if that account is not signed in. Omit for the first signed-in account.
- `all_day` (boolean, optional): Convert to/from all-day
- `location` (string, optional)
- `add_guests` (array, optional): Guest emails to add (an invitation is emailed to each)
- `description` (string, optional)

## Output

- `eid` (string, required)
- `changed` (array, required)
- `updated` (boolean, required)
- `account` (string | null, optional): Email of the Google account the event was edited as.

## FAQ

### What does "Update a Google Calendar event" do?

Edit an existing Google Calendar event by its eid (from list_events/search_events/create_event). Opens the event composer and applies only the fields you pass — title, start, end (ISO datetime, or YYYY-MM-DD with all_day), all_day, location, description, add_guests — then Saves, sending update/invitation emails to guests when present. Single (non-recurring) events; a recurring instance's this/all scope dialog isn't handled. Changing start alone shifts the end to keep the duration unless you also pass end.

### How do I automatically update a Google Calendar event on calendar.google.com?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/update_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/update_event

### Is there a calendar.google.com API to update a Google Calendar event?

You do not need one. "Update a Google Calendar event" drives the real calendar.google.com pages in a browser, so it works whether or not calendar.google.com offers an API for this.

### What information do I need to provide?

Required: eid. Optional: end, start, title, account, all_day, location, add_guests, description.

### What does it return?

It returns eid, account, changed, updated.

### Do I need to be logged in to calendar.google.com?

Yes. It acts as you on calendar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendar.google.com cookies saved by the Reduck extension.

### Does it change anything on calendar.google.com, or only read data?

It makes changes on calendar.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/update_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/update_event

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendar.google.com/update_event
