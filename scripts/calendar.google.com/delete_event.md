# Delete a Google Calendar event

Automatically delete a Google Calendar event on calendar.google.com. Delete an event from the signed-in Google Calendar by its eid (the handle returned by list_events / create_event) or an event link. Guests are sent a cancellation notice. Single (non-recurring) events only; a recurring event is not supported. Irreversible.

- Site: calendar.google.com
- Address: `reduck/calendar.google.com/delete_event`
- Updated: 2026-11-02 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendar.google.com/delete_event`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/delete_event
```

## Input

- `eid` (string, required): The event's eid (from list_events, search_events or create_event), or a Google Calendar event link that carries it (…/eventedit/<eid> or …?eid=<eid>).
- `account` (string, optional): The Google account to delete as, when this browser is signed in to several: its email, or its number in this browser ("1"), as mail.google.com/list_accounts lists them. Use the account the eid came from. The run fails, deleting nothing, if that account is not signed in. Omit for the first signed-in account.

## Output

- `eid` (string, required)
- `deleted` (boolean, required)
- `account` (string | null, optional): Email of the Google account the event was deleted as.

## FAQ

### What does "Delete a Google Calendar event" do?

Delete an event from the signed-in Google Calendar by its eid (the handle returned by list_events / create_event) or an event link. Guests are sent a cancellation notice. Single (non-recurring) events only; a recurring event is not supported. Irreversible.

### How do I automatically delete a Google Calendar event on calendar.google.com?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/delete_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/delete_event

### Is there a calendar.google.com API to delete a Google Calendar event?

You do not need one. "Delete a Google Calendar event" drives the real calendar.google.com pages in a browser, so it works whether or not calendar.google.com offers an API for this.

### What information do I need to provide?

Required: eid. Optional: account.

### What does it return?

It returns eid, account, deleted.

### Do I need to be logged in to calendar.google.com?

Yes. It acts as you on calendar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendar.google.com cookies saved by the Reduck extension.

### Does it change anything on calendar.google.com, or only read data?

It makes changes on calendar.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/delete_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/delete_event

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendar.google.com/delete_event
