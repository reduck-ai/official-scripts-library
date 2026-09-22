# Delete a Google Calendar event

Automatically delete a Google Calendar event on calendar.google.com. Delete an event from the signed-in Google Calendar by its eid (the base64 handle returned by list_events / create_event). Opens the event in the composer, uses More actions > Delete, sends a cancellation notice to any guests, and confirms by leaving the composer route. Single (non-recurring) events only — a recurring instance pops a this/all scope dialog this v1 doesn't handle. Irreversible.

- Site: calendar.google.com
- Address: `reduck/calendar.google.com/delete_event`
- Updated: 2026-08-27 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendar.google.com/delete_event`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/delete_event
```

## Input

- `eid` (string, required)

## Output

- `eid` (string, required)
- `deleted` (boolean, required)

## FAQ

### What does "Delete a Google Calendar event" do?

Delete an event from the signed-in Google Calendar by its eid (the base64 handle returned by list_events / create_event). Opens the event in the composer, uses More actions > Delete, sends a cancellation notice to any guests, and confirms by leaving the composer route. Single (non-recurring) events only — a recurring instance pops a this/all scope dialog this v1 doesn't handle. Irreversible.

### How do I automatically delete a Google Calendar event on calendar.google.com?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/delete_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/delete_event

### Is there a calendar.google.com API to delete a Google Calendar event?

You do not need one. "Delete a Google Calendar event" drives the real calendar.google.com pages in a browser, so it works whether or not calendar.google.com offers an API for this.

### What information do I need to provide?

Required: eid.

### What does it return?

It returns eid, deleted.

### Do I need to be logged in to calendar.google.com?

Yes. It acts as you on calendar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendar.google.com cookies saved by the Reduck extension.

### Does it change anything on calendar.google.com, or only read data?

It makes changes on calendar.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/delete_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/delete_event

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendar.google.com/delete_event
