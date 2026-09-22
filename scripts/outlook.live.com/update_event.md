# Update calendar event (Outlook)

Automatically update calendar event (Outlook) on outlook.live.com. Edit an existing event in the signed-in Outlook consumer calendar, by its event id. Changes subject, body, and location (the last only on an event that has none). Requires the expected subject as a safety interlock, and confirms every change by reloading the event, because this calendar sometimes reverts a write. Start and end times cannot be changed.

- Site: outlook.live.com
- Address: `reduck/outlook.live.com/update_event`
- Updated: 2026-09-18 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/outlook.live.com/update_event`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/update_event
```

## Input

- `eventId` (string, required): The event's data-calitemid, as returned by list_events.
- `expectedSubject` (string, required): The subject the event currently has. Safety interlock: if the event on the page does not match, nothing is edited.
- `body` (string, optional): New body text, replacing what is there. Omit to leave unchanged.
- `subject` (string, optional): New subject. Omit to leave unchanged.
- `location` (string, optional): New location. Only settable on an event that has none: Outlook's location box adds a second entry rather than replacing the first, and the existing chip cannot be cleared from here, so replacing one is refused rather than leaving the event carrying two. Omit to leave unchanged.

## Output

- `after` (object, required)
- `before` (object, required)
- `changed` (array, required): Which fields were confirmed different after reloading the event.
- `eventId` (string, required)
- `updated` (boolean, required)

## FAQ

### What does "Update calendar event (Outlook)" do?

Edit an existing event in the signed-in Outlook consumer calendar, by its event id. Changes subject, body, and location (the last only on an event that has none). Requires the expected subject as a safety interlock, and confirms every change by reloading the event, because this calendar sometimes reverts a write. Start and end times cannot be changed.

### How do I automatically update calendar event (Outlook) on outlook.live.com?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/update_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/update_event

### Is there a outlook.live.com API to update calendar event (Outlook)?

You do not need one. "Update calendar event (Outlook)" drives the real outlook.live.com pages in a browser, so it works whether or not outlook.live.com offers an API for this.

### What information do I need to provide?

Required: eventId, expectedSubject. Optional: body, subject, location.

### What does it return?

It returns after, before, changed, eventId, updated.

### Do I need to be logged in to outlook.live.com?

Yes. It acts as you on outlook.live.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the outlook.live.com cookies saved by the Reduck extension.

### Does it change anything on outlook.live.com, or only read data?

It makes changes on outlook.live.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/update_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/update_event

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/outlook.live.com/update_event
