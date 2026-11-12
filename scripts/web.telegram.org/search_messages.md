# Search Telegram messages

Automatically search Telegram messages on web.telegram.org. Search Telegram messages by words, in one conversation (a peer id or a public @username) or in all conversations of the account. Returns up to 20 messages a page, newest first, with their conversation, id, date, sender and full text; the ids work with download_media and delete_message. Takes optional date bounds; pass nextCursor for the next page. An empty list means that nothing matched. Searching does not mark anything as read.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/search_messages`
- Updated: 2026-11-11 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/search_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/search_messages
```

## Input

- `query` (string, required): The words to search for.
- `cursor` (string, optional): Omit for the first page. For the next one, pass the nextCursor of the previous call with the same query, peerId and dates.
- `peerId` (string, optional): Search only this conversation: its peerId from web.telegram.org/get_inbox, or a public @username (such as "@telegram"). Omit to search every conversation of the account.
- `maxDate` (string, optional): Only messages sent before this time, ISO 8601.
- `minDate` (string, optional): Only messages sent at or after this time, ISO 8601 (e.g. "2026-01-01").

## Output

- `results` (array, required): Up to 20 matching messages, newest first. Empty when nothing matches.
- `nextCursor` (string | null, required): Pass it as cursor for the next page. Null on the last page.
- `totalCount` (integer | null, optional): How many messages match in all.

## FAQ

### What does "Search Telegram messages" do?

Search Telegram messages by words, in one conversation (a peer id or a public @username) or in all conversations of the account. Returns up to 20 messages a page, newest first, with their conversation, id, date, sender and full text; the ids work with download_media and delete_message. Takes optional date bounds; pass nextCursor for the next page. An empty list means that nothing matched. Searching does not mark anything as read.

### How do I automatically search Telegram messages on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/search_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/search_messages

### Is there a web.telegram.org API to search Telegram messages?

You do not need one. "Search Telegram messages" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Required: query. Optional: cursor, peerId, maxDate, minDate.

### What does it return?

It returns results, nextCursor, totalCount.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It only reads. It looks things up on web.telegram.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/search_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/search_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/search_messages
