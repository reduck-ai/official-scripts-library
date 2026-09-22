# Delete calendar event (Outlook)

Automatically delete calendar event (Outlook) on outlook.live.com. Delete a single event from the signed-in Outlook consumer calendar, identified by its event id. Requires the expected subject as a safety interlock, and verifies the deletion committed by reloading — the site sometimes reverts a delete.

- Site: outlook.live.com
- Address: `reduck/outlook.live.com/delete_event`
- Updated: 2026-09-16 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/outlook.live.com/delete_event`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/delete_event
```

## Input

- `date` (string, required): The event's date (YYYY-MM-DD), used to navigate to its week.
- `eventId` (string, required): The event's data-calitemid, as returned by list_events.
- `expectedSubject` (string, required): The subject you expect this event to have. Safety interlock: if the event on the page does not match, nothing is deleted.

## Output

- `date` (string, required)
- `deleted` (boolean, required)
- `eventId` (string, required)
- `subject` (string, required)
- `countAfter` (integer, required)
- `countBefore` (integer, required)

## FAQ

### What does "Delete calendar event (Outlook)" do?

Delete a single event from the signed-in Outlook consumer calendar, identified by its event id. Requires the expected subject as a safety interlock, and verifies the deletion committed by reloading — the site sometimes reverts a delete.

### How do I automatically delete calendar event (Outlook) on outlook.live.com?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/delete_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/delete_event

### Is there a outlook.live.com API to delete calendar event (Outlook)?

You do not need one. "Delete calendar event (Outlook)" drives the real outlook.live.com pages in a browser, so it works whether or not outlook.live.com offers an API for this.

### What information do I need to provide?

Required: eventId, date, expectedSubject.

### What does it return?

It returns date, deleted, eventId, subject, countAfter, countBefore.

### Do I need to be logged in to outlook.live.com?

Yes. It acts as you on outlook.live.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the outlook.live.com cookies saved by the Reduck extension.

### Does it change anything on outlook.live.com, or only read data?

It makes changes on outlook.live.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/delete_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/delete_event

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/outlook.live.com/delete_event
