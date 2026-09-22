# Create calendar event (Outlook)

Automatically create calendar event (Outlook) on outlook.live.com. Create an event in the signed-in Outlook consumer calendar.

- Site: outlook.live.com
- Address: `reduck/outlook.live.com/create_event`
- Updated: 2026-09-16 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/outlook.live.com/create_event`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/create_event
```

## Input

- `end` (string, required): End as local ISO, e.g. 2026-09-17T10:30:00.
- `start` (string, required): Start as local ISO, e.g. 2026-09-17T10:00:00. Passed to the deeplink verbatim; the site renders it in the mailbox locale.
- `subject` (string, required): Event title. Required — it is also the read-back oracle.
- `body` (string, optional): Optional event body text.
- `location` (string, optional): Optional location. Typed into the picker — the deeplink's location param is ignored by the site.

## Output

- `end` (string, required)
- `start` (string, required)
- `created` (boolean, required)
- `subject` (string, required)
- `verified` (boolean, required)
- `locationSet` (boolean, optional)
- `renderedWhen` (string, optional): The composer's own rendering of the date range, as confirmation the ISO input was understood.
- `unverifiedReason` (string, optional)

## FAQ

### What does "Create calendar event (Outlook)" do?

Create an event in the signed-in Outlook consumer calendar.

### How do I automatically create calendar event (Outlook) on outlook.live.com?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/create_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/create_event

### Is there a outlook.live.com API to create calendar event (Outlook)?

You do not need one. "Create calendar event (Outlook)" drives the real outlook.live.com pages in a browser, so it works whether or not outlook.live.com offers an API for this.

### What information do I need to provide?

Required: subject, start, end. Optional: body, location.

### What does it return?

It returns end, start, created, subject, verified, locationSet, renderedWhen, unverifiedReason.

### Do I need to be logged in to outlook.live.com?

Yes. It acts as you on outlook.live.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the outlook.live.com cookies saved by the Reduck extension.

### Does it change anything on outlook.live.com, or only read data?

It makes changes on outlook.live.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/create_event, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/create_event

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/outlook.live.com/create_event
