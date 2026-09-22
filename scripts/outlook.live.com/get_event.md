# Get calendar event (Outlook)

Automatically get calendar event (Outlook) on outlook.live.com. Read the full detail of one event in the signed-in Outlook consumer calendar, by its event id.

- Site: outlook.live.com
- Address: `reduck/outlook.live.com/get_event`
- Updated: 2026-09-16 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/outlook.live.com/get_event`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/get_event
```

## Input

- `eventId` (string, required): The event's data-calitemid, as returned by list_events.

## Output

- `id` (string, required)
- `url` (string, required)
- `body` (string, required): Empty string when the event has no body.
- `when` (string, required): The site's own rendering of the date range, verbatim and LOCALE-DEPENDENT (e.g. 'Fri 18/09/2026 14:00 - 15:00'). Deliberately not parsed into a date: dd/mm and mm/dd are indistinguishable here, so use list_events for the ISO date.
- `subject` (string, required)
- `location` (string, required): Empty string when the event has no location.
- `endTime` (string, optional): End time HH:MM. Empty if not parseable.
- `attendees` (string, optional): Required attendees as rendered, empty when there are none.
- `startTime` (string, optional): Start time HH:MM, taken from digits so it survives translation. Empty if not parseable.

## FAQ

### What does "Get calendar event (Outlook)" do?

Read the full detail of one event in the signed-in Outlook consumer calendar, by its event id.

### How do I automatically get calendar event (Outlook) on outlook.live.com?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/get_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/get_event

### Is there a outlook.live.com API to get calendar event (Outlook)?

You do not need one. "Get calendar event (Outlook)" drives the real outlook.live.com pages in a browser, so it works whether or not outlook.live.com offers an API for this.

### What information do I need to provide?

Required: eventId.

### What does it return?

It returns id, url, body, when, endTime, subject, location, attendees, startTime.

### Do I need to be logged in to outlook.live.com?

Yes. It acts as you on outlook.live.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the outlook.live.com cookies saved by the Reduck extension.

### Does it change anything on outlook.live.com, or only read data?

It only reads. It looks things up on outlook.live.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/get_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/get_event

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/outlook.live.com/get_event
