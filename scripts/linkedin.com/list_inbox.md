# List LinkedIn message inbox

Automatically list LinkedIn message inbox on linkedin.com. List the classic LinkedIn messaging inbox conversations (NOT Sales Navigator). Returns each conversation's thread URL/id, counterpart participants (name, profileUrl), unread count, last activity, and last message (text, time, fromSelf, subject). Paginates: a limit above 20 scrolls the inbox to load older conversations, and sinceIso fetches everything back to a given date (e.g. the last N months).

- Site: linkedin.com
- Address: `reduck/linkedin.com/list_inbox`
- Updated: 2026-09-03 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/list_inbox`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/list_inbox
```

## Input

- `limit` (number, optional): Max conversations to return, newest first. Up to 20 come from the first page with no scrolling; a higher limit scrolls the inbox to load older conversations until this many are collected (or the inbox is exhausted).
- `sinceIso` (string, optional): Optional ISO date/datetime (e.g. "2026-03-28"). Keep scrolling until conversations older than this are reached, and drop any conversation whose last activity is before it. Use to fetch a time window (e.g. the last N months) without guessing a limit.
- `unreadOnly` (boolean, optional): Only return conversations with unread messages. Default false.

## Output

- `count` (number, required)
- `conversations` (array, required)
- `exhausted` (boolean, optional)
- `pagesLoaded` (number, optional)

## FAQ

### What does "List LinkedIn message inbox" do?

List the classic LinkedIn messaging inbox conversations (NOT Sales Navigator). Returns each conversation's thread URL/id, counterpart participants (name, profileUrl), unread count, last activity, and last message (text, time, fromSelf, subject). Paginates: a limit above 20 scrolls the inbox to load older conversations, and sinceIso fetches everything back to a given date (e.g. the last N months).

### How do I automatically list LinkedIn message inbox on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/list_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/list_inbox

### Is there a linkedin.com API to list LinkedIn message inbox?

You do not need one. "List LinkedIn message inbox" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: limit, sinceIso, unreadOnly.

### What does it return?

It returns count, exhausted, pagesLoaded, conversations.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/list_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/list_inbox

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/list_inbox
