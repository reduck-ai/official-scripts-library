# List calendars (Outlook)

Automatically list calendars (Outlook) on outlook.live.com. List the calendars in the signed-in Outlook consumer mailbox, with their shown/hidden state. Covers a single-calendar lookup by filtering on name.

- Site: outlook.live.com
- Address: `reduck/outlook.live.com/list_calendars`
- Updated: 2026-09-16 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/outlook.live.com/list_calendars`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/list_calendars
```

## Input

- `name` (string, optional): Optional. Return only the calendar whose name matches this exactly (case-insensitive). This is how a single-calendar 'get' is served — there is no separate get script.

## Output

- `count` (integer, required)
- `calendars` (array, required)
- `expandedRail` (boolean, required): Whether the rail's show-all expander was clicked. False means every calendar was already visible OR the expander could not be found — in the latter case the list may be limited to ticked calendars.

## FAQ

### What does "List calendars (Outlook)" do?

List the calendars in the signed-in Outlook consumer mailbox, with their shown/hidden state. Covers a single-calendar lookup by filtering on name.

### How do I automatically list calendars (Outlook) on outlook.live.com?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/list_calendars, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/list_calendars

### Is there a outlook.live.com API to list calendars (Outlook)?

You do not need one. "List calendars (Outlook)" drives the real outlook.live.com pages in a browser, so it works whether or not outlook.live.com offers an API for this.

### What information do I need to provide?

Optional: name.

### What does it return?

It returns count, calendars, expandedRail.

### Do I need to be logged in to outlook.live.com?

Yes. It acts as you on outlook.live.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the outlook.live.com cookies saved by the Reduck extension.

### Does it change anything on outlook.live.com, or only read data?

It only reads. It looks things up on outlook.live.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/list_calendars, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/list_calendars

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/outlook.live.com/list_calendars
