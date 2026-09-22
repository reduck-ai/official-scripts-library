# RSVP to a Google Calendar invitation

Respond to a Google Calendar invitation (RSVP yes / no / maybe) by its eid, as the signed-in account. Opens the event, sets the Going? response and saves; the organizer is notified automatically. Only works on events you were invited to (that expose the RSVP control) — passing an event you solely organize fails loudly. Returns responded, eid, response.

- Site: calendar.google.com
- Address: `reduck/calendar.google.com/respond_invitation`
- Updated: 2026-08-27 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendar.google.com/respond_invitation`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/respond_invitation
```

## Input

- `eid` (string, required): Base64 event handle from list_events/search_events
- `response` (string, required): RSVP response

## Output

- `eid` (string, required)
- `response` (string, required)
- `responded` (boolean, required)

## FAQ

### What does "RSVP to a Google Calendar invitation" do?

Respond to a Google Calendar invitation (RSVP yes / no / maybe) by its eid, as the signed-in account. Opens the event, sets the Going? response and saves; the organizer is notified automatically. Only works on events you were invited to (that expose the RSVP control) — passing an event you solely organize fails loudly. Returns responded, eid, response.

### What information do I need to provide?

Required: eid, response.

### What does it return?

It returns eid, response, responded.

### Do I need to be logged in to calendar.google.com?

Yes. It acts as you on calendar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendar.google.com cookies saved by the Reduck extension.

### Does it change anything on calendar.google.com, or only read data?

It makes changes on calendar.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/respond_invitation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/respond_invitation

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendar.google.com/respond_invitation
