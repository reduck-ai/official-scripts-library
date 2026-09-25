# Set Out of Office

Automatically set Out of Office on calendar.google.com. Create an out-of-office entry on the signed-in Google Calendar's primary calendar for a date range, with an optional custom decline message. New and existing meetings in that range are declined automatically unless declineMeetings is set false. A rehearsal mode fills the entry in and stops before saving.

- Site: calendar.google.com
- Address: `reduck/calendar.google.com/set_out_of_office`
- Updated: 2026-09-24 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendar.google.com/set_out_of_office`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/set_out_of_office
```

## Input

- `endDate` (string, required): End date, YYYY-MM-DD (inclusive)
- `startDate` (string, required): Start date, YYYY-MM-DD (inclusive)
- `dry_run` (boolean, optional): When true the entry is filled in — dates, decline setting and message — and the run stops on the step before the one that saves it. Nothing is written, and saved comes back false.
- `message` (string, optional): Custom decline message. Omit to keep Google's own default wording.
- `declineMeetings` (boolean, optional): Automatically decline new and existing meetings during this time. Defaults to true, matching Google Calendar's own default. Declining notifies the people who invited you.

## Output

- `saved` (boolean, required): True once the composer closed after saving, and after confirming the decline when meetings are being declined.
- `endDate` (string, required)
- `startDate` (string, required)
- `dryRun` (boolean, optional)
- `message` (string | null, optional): The custom decline message this run was asked to set, or null when Google's default wording was kept.
- `composerReady` (boolean, optional)
- `messageApplied` (boolean, optional): Whether the message was read back from the field and matched just before saving. Google does not show the decline message anywhere after saving, so this is the furthest it can be checked; it does not prove the server kept it.
- `declineMeetings` (boolean, optional)

## FAQ

### What does "Set Out of Office" do?

Create an out-of-office entry on the signed-in Google Calendar's primary calendar for a date range, with an optional custom decline message. New and existing meetings in that range are declined automatically unless declineMeetings is set false. A rehearsal mode fills the entry in and stops before saving.

### How do I automatically set Out of Office on calendar.google.com?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/set_out_of_office, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/set_out_of_office

### Is there a calendar.google.com API to set Out of Office?

You do not need one. "Set Out of Office" drives the real calendar.google.com pages in a browser, so it works whether or not calendar.google.com offers an API for this.

### What information do I need to provide?

Required: startDate, endDate. Optional: dry_run, message, declineMeetings.

### What does it return?

It returns saved, dryRun, endDate, message, startDate, composerReady, messageApplied, declineMeetings.

### Do I need to be logged in to calendar.google.com?

Yes. It acts as you on calendar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendar.google.com cookies saved by the Reduck extension.

### Does it change anything on calendar.google.com, or only read data?

It makes changes on calendar.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/set_out_of_office, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/set_out_of_office

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendar.google.com/set_out_of_office
