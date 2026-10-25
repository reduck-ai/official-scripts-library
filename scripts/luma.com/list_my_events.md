# List my Luma events (upcoming or past)

Automatically list my Luma events (upcoming or past) on luma.com. List the events on the signed-in Luma account's own Events page: the upcoming ones, or the past ones, one page at a time. Each event says whether you are a guest, a host or a manager, your registration status (e.g. approved, pending), when and where it is, who hosts it, its guest count, and whether its guest list is visible. When has_more is true, pass next_cursor as cursor to get the next page.

- Site: luma.com
- Address: `reduck/luma.com/list_my_events`
- Updated: 2026-10-23 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/luma.com/list_my_events`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/luma.com/list_my_events
```

## Input

- `limit` (integer, optional): Max events to return per page. Default 25.
- `cursor` (string, optional): next_cursor from a previous run with the same period, to get the next page.
- `period` (string, optional): Which tab of your Events page: "future" (Upcoming, the default) or "past".

## Output

- `events` (array, required)
- `period` (string, required)
- `account` (string, required): The signed-in Luma account's email: whose events these are.
- `has_more` (boolean, required): True when the account has more events in this period after this page.
- `next_cursor` (string | null, required): Pass as cursor to get the next page; null on the last page.

## FAQ

### What does "List my Luma events (upcoming or past)" do?

List the events on the signed-in Luma account's own Events page: the upcoming ones, or the past ones, one page at a time. Each event says whether you are a guest, a host or a manager, your registration status (e.g. approved, pending), when and where it is, who hosts it, its guest count, and whether its guest list is visible. When has_more is true, pass next_cursor as cursor to get the next page.

### How do I automatically list my Luma events (upcoming or past) on luma.com?

Ask an AI agent connected to Reduck to run reduck/luma.com/list_my_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/list_my_events

### Is there a luma.com API to list my Luma events (upcoming or past)?

You do not need one. "List my Luma events (upcoming or past)" drives the real luma.com pages in a browser, so it works whether or not luma.com offers an API for this.

### What information do I need to provide?

Optional: limit, cursor, period.

### What does it return?

It returns events, period, account, has_more, next_cursor.

### Do I need to be logged in to luma.com?

Yes. It acts as you on luma.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the luma.com cookies saved by the Reduck extension.

### Does it change anything on luma.com, or only read data?

It only reads. It looks things up on luma.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/luma.com/list_my_events, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/list_my_events

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/luma.com/list_my_events
