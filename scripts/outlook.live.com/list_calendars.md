# List Outlook.com calendars

Automatically list Outlook.com calendars on outlook.live.com. List every calendar in the signed-in Outlook.com mailbox, ticked on or not, with whether each is shown in the calendar view and its colour (empty when set to automatic).

- Site: outlook.live.com
- Address: `reduck/outlook.live.com/list_calendars`
- Updated: 2026-10-28 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/outlook.live.com/list_calendars`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/list_calendars
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `calendars` (array, required)
- `expandedRail` (boolean, required): Always false: every calendar is listed, ticked or not. Kept for existing callers.

## FAQ

### What does "List Outlook.com calendars" do?

List every calendar in the signed-in Outlook.com mailbox, ticked on or not, with whether each is shown in the calendar view and its colour (empty when set to automatic).

### How do I automatically list Outlook.com calendars on outlook.live.com?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/list_calendars, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/list_calendars

### Is there a outlook.live.com API to list Outlook.com calendars?

You do not need one. "List Outlook.com calendars" drives the real outlook.live.com pages in a browser, so it works whether or not outlook.live.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

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
