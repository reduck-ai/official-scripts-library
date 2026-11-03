# Add Google Meet link to a Calendar event

Automatically add Google Meet link to a Calendar event on calendar.google.com. Add a Google Meet video-conferencing link to an existing Google Calendar event, by its eid. Safe to repeat: if the event already has a conference link, nothing changes and the existing link is returned. Returns the event's Meet link, verified by reopening the saved event.

- Site: calendar.google.com
- Address: `reduck/calendar.google.com/add_conference_link`
- Updated: 2026-11-02 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendar.google.com/add_conference_link`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/add_conference_link
```

## Input

- `eid` (string, required): Event handle from list_events, search_events or create_event
- `account` (string, optional): The Google account to edit as, when this browser is signed in to several: its email, or its number in this browser ("1"), as mail.google.com/list_accounts lists them. Use the account the eid came from. The run fails, changing nothing, if that account is not signed in. Omit for the first signed-in account.

## Output

- `eid` (string, required)
- `added` (boolean, required): true if a new link was added; false if the event already had one
- `meetLink` (string, required)
- `account` (string | null, optional): Email of the Google account the link was added as.

## FAQ

### What does "Add Google Meet link to a Calendar event" do?

Add a Google Meet video-conferencing link to an existing Google Calendar event, by its eid. Safe to repeat: if the event already has a conference link, nothing changes and the existing link is returned. Returns the event's Meet link, verified by reopening the saved event.

### How do I automatically add Google Meet link to a Calendar event on calendar.google.com?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/add_conference_link, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/add_conference_link

### Is there a calendar.google.com API to add Google Meet link to a Calendar event?

You do not need one. "Add Google Meet link to a Calendar event" drives the real calendar.google.com pages in a browser, so it works whether or not calendar.google.com offers an API for this.

### What information do I need to provide?

Required: eid. Optional: account.

### What does it return?

It returns eid, added, account, meetLink.

### Do I need to be logged in to calendar.google.com?

Yes. It acts as you on calendar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendar.google.com cookies saved by the Reduck extension.

### Does it change anything on calendar.google.com, or only read data?

It makes changes on calendar.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/add_conference_link, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/add_conference_link

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendar.google.com/add_conference_link
