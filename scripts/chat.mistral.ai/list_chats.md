# List Le Chat conversations

Automatically list Le Chat conversations on chat.mistral.ai. List recent Le Chat conversations, newest first.

- Site: chat.mistral.ai
- Address: `reduck/chat.mistral.ai/list_chats`
- Updated: 2026-09-02 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chat.mistral.ai/list_chats`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/list_chats
```

## Input

- `limit` (integer, optional): Max conversations to return, newest first

## Output

- `items` (array, required)

## FAQ

### What does "List Le Chat conversations" do?

List recent Le Chat conversations, newest first.

### How do I automatically list Le Chat conversations on chat.mistral.ai?

Ask an AI agent connected to Reduck to run reduck/chat.mistral.ai/list_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/list_chats

### Is there a chat.mistral.ai API to list Le Chat conversations?

You do not need one. "List Le Chat conversations" drives the real chat.mistral.ai pages in a browser, so it works whether or not chat.mistral.ai offers an API for this.

### What information do I need to provide?

Optional: limit.

### What does it return?

It returns items.

### Do I need to be logged in to chat.mistral.ai?

Yes. It acts as you on chat.mistral.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the chat.mistral.ai cookies saved by the Reduck extension.

### Does it change anything on chat.mistral.ai, or only read data?

It only reads. It looks things up on chat.mistral.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chat.mistral.ai/list_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/list_chats

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chat.mistral.ai/list_chats
