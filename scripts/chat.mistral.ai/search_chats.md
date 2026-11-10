# Search Le Chat conversations

Automatically search Le Chat conversations on chat.mistral.ai. Search the text of all your Le Chat conversations. Returns each matching message with its conversation id and title, role, time and an excerpt with the matched words in bold. Pass nextCursor back as cursor for more.

- Site: chat.mistral.ai
- Address: `reduck/chat.mistral.ai/search_chats`
- Updated: 2026-11-09 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chat.mistral.ai/search_chats`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/search_chats
```

## Input

- `query` (string, required): Search query, matched against message content across all conversations
- `cursor` (integer | null, optional): nextCursor from the previous call, for the next page of matches.

## Output

- `items` (array, required)
- `nextCursor` (integer | null, required): Pass as cursor for the next page of matches.

## FAQ

### What does "Search Le Chat conversations" do?

Search the text of all your Le Chat conversations. Returns each matching message with its conversation id and title, role, time and an excerpt with the matched words in bold. Pass nextCursor back as cursor for more.

### How do I automatically search Le Chat conversations on chat.mistral.ai?

Ask an AI agent connected to Reduck to run reduck/chat.mistral.ai/search_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/search_chats

### Is there a chat.mistral.ai API to search Le Chat conversations?

You do not need one. "Search Le Chat conversations" drives the real chat.mistral.ai pages in a browser, so it works whether or not chat.mistral.ai offers an API for this.

### What information do I need to provide?

Required: query. Optional: cursor.

### What does it return?

It returns items, nextCursor.

### Do I need to be logged in to chat.mistral.ai?

Yes. It acts as you on chat.mistral.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the chat.mistral.ai cookies saved by the Reduck extension.

### Does it change anything on chat.mistral.ai, or only read data?

It only reads. It looks things up on chat.mistral.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chat.mistral.ai/search_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/search_chats

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chat.mistral.ai/search_chats
