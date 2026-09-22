# Add Google Meet link to a Calendar event

Automatically add Google Meet link to a Calendar event on calendar.google.com. Add a Google Meet video-conferencing link to an existing Google Calendar event, by its eid. Safe to repeat: if the event already has a conference link, nothing changes and the existing link is returned. Returns the event's Meet link, verified by reopening the saved event.

- Site: calendar.google.com
- Address: `reduck/calendar.google.com/add_conference_link`
- Updated: 2026-09-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendar.google.com/add_conference_link`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/add_conference_link
```

## Input

- `eid` (string, required): Base64 event handle from list_events/search_events/create_event

## Output

- `eid` (string, required)
- `added` (boolean, required): true if a new link was added; false if the event already had one
- `meetLink` (string, required)

## FAQ

### What does "Add Google Meet link to a Calendar event" do?

Add a Google Meet video-conferencing link to an existing Google Calendar event, by its eid. Safe to repeat: if the event already has a conference link, nothing changes and the existing link is returned. Returns the event's Meet link, verified by reopening the saved event.

### How do I automatically add Google Meet link to a Calendar event on calendar.google.com?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/add_conference_link, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/add_conference_link

### Is there a calendar.google.com API to add Google Meet link to a Calendar event?

You do not need one. "Add Google Meet link to a Calendar event" drives the real calendar.google.com pages in a browser, so it works whether or not calendar.google.com offers an API for this.

### What information do I need to provide?

Required: eid.

### What does it return?

It returns eid, added, meetLink.

### Do I need to be logged in to calendar.google.com?

Yes. It acts as you on calendar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendar.google.com cookies saved by the Reduck extension.

### Does it change anything on calendar.google.com, or only read data?

It makes changes on calendar.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/add_conference_link, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/add_conference_link

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendar.google.com/add_conference_link
