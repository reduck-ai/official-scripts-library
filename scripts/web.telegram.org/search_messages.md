# Search Telegram messages in a conversation

Automatically search Telegram messages in a conversation on web.telegram.org. Search inside one Telegram conversation using the conversation's own search box, and return the matching messages: the chat they are in, the date label shown on the result, and the matched text. Returns an empty list when nothing matches, which is a real answer. Note the result rows carry no message id, so results cannot be fed straight to delete or react — use get_conversation for ids. Searching across all chats is a separate Telegram surface and is not covered here.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/search_messages`
- Updated: 2026-09-16 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/search_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/search_messages
```

## Input

- `query` (string, required): The text to search for inside the conversation.
- `peerId` (string, required): The conversation to search in, as returned by get_inbox. Required — this script drives the per-conversation search box, not Telegram's global search.
- `count` (integer, optional): Maximum results to return from what the search dropdown has rendered.

## Output

- `count` (integer, required): How many results were returned.
- `query` (string, required): The query that was searched.
- `peerId` (string, required): The peer id that was searched, read back from the address bar.
- `results` (array, required): Matching messages in the order the search dropdown lists them (most recent first). Empty when nothing matched.
- `chatTitle` (string | null, optional): The conversation title from the header, for a human-readable cross-check against peerId.

## FAQ

### What does "Search Telegram messages in a conversation" do?

Search inside one Telegram conversation using the conversation's own search box, and return the matching messages: the chat they are in, the date label shown on the result, and the matched text. Returns an empty list when nothing matches, which is a real answer. Note the result rows carry no message id, so results cannot be fed straight to delete or react — use get_conversation for ids. Searching across all chats is a separate Telegram surface and is not covered here.

### How do I automatically search Telegram messages in a conversation on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/search_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/search_messages

### Is there a web.telegram.org API to search Telegram messages in a conversation?

You do not need one. "Search Telegram messages in a conversation" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Required: peerId, query. Optional: count.

### What does it return?

It returns count, query, peerId, results, chatTitle.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It only reads. It looks things up on web.telegram.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/search_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/search_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/search_messages
