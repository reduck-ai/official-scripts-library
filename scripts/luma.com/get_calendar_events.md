# Get events from a Luma calendar

Automatically get events from a Luma calendar on luma.com. List the past or future events published under a specific Luma calendar/organizer (e.g. "AITinkerers"), paginated.

- Site: luma.com
- Address: `reduck/luma.com/get_calendar_events`
- Updated: 2026-09-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/luma.com/get_calendar_events`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/luma.com/get_calendar_events
```

## Input

- `calendar` (string, required): The calendar's Luma handle, e.g. "AITinkerers" from luma.com/AITinkerers.
- `limit` (integer, optional): Max events to return per call. Default 25.
- `cursor` (string, optional): Pagination cursor from a previous call's next_cursor.
- `period` (string, optional): Which set of events to list. Default "future".

## Output

- `events` (array, required)
- `calendar` (object, required)
- `has_more` (boolean, required)
- `next_cursor` (string | null, optional)

## FAQ

### What does "Get events from a Luma calendar" do?

List the past or future events published under a specific Luma calendar/organizer (e.g. "AITinkerers"), paginated.

### How do I automatically get events from a Luma calendar on luma.com?

Ask an AI agent connected to Reduck to run reduck/luma.com/get_calendar_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/get_calendar_events

### Is there a luma.com API to get events from a Luma calendar?

You do not need one. "Get events from a Luma calendar" drives the real luma.com pages in a browser, so it works whether or not luma.com offers an API for this.

### What information do I need to provide?

Required: calendar. Optional: limit, cursor, period.

### What does it return?

It returns events, calendar, has_more, next_cursor.

### Do I need to be logged in to luma.com?

No. It only uses pages of luma.com that are reachable without signing in.

### Does it change anything on luma.com, or only read data?

It only reads. It looks things up on luma.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/luma.com/get_calendar_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/get_calendar_events

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/luma.com/get_calendar_events
