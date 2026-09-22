# List calendar events (Outlook)

Automatically list calendar events (Outlook) on outlook.live.com. List events from the signed-in Outlook consumer calendar for a given week.

- Site: outlook.live.com
- Address: `reduck/outlook.live.com/list_events`
- Updated: 2026-09-16 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/outlook.live.com/list_events`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/list_events
```

## Input

- `date` (string, optional): Any date in the target week (YYYY-MM-DD). Omitted = the current week.

## Output

- `days` (array, required)
- `count` (integer, required)
- `events` (array, required)
- `weekEnd` (string, required)
- `weekStart` (string, required)

## FAQ

### What does "List calendar events (Outlook)" do?

List events from the signed-in Outlook consumer calendar for a given week.

### How do I automatically list calendar events (Outlook) on outlook.live.com?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/list_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/list_events

### Is there a outlook.live.com API to list calendar events (Outlook)?

You do not need one. "List calendar events (Outlook)" drives the real outlook.live.com pages in a browser, so it works whether or not outlook.live.com offers an API for this.

### What information do I need to provide?

Optional: date.

### What does it return?

It returns days, count, events, weekEnd, weekStart.

### Do I need to be logged in to outlook.live.com?

Yes. It acts as you on outlook.live.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the outlook.live.com cookies saved by the Reduck extension.

### Does it change anything on outlook.live.com, or only read data?

It only reads. It looks things up on outlook.live.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/list_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/list_events

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/outlook.live.com/list_events
