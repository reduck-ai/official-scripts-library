# Delete Le Chat conversation

Automatically delete Le Chat conversation on chat.mistral.ai. Delete one Le Chat conversation by id (moves it to trash; Le Chat purges trashed conversations automatically after 30 days).

- Site: chat.mistral.ai
- Address: `reduck/chat.mistral.ai/delete_chat`
- Updated: 2026-08-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chat.mistral.ai/delete_chat`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/delete_chat
```

## Input

- `chatId` (string, required): Conversation id to delete, from list_chats or search_chats

## Output

- `title` (string, required)
- `chatId` (string, required)
- `status` (string, required): Le Chat's status for the conversation after this call, e.g. "deleted"

## FAQ

### What does "Delete Le Chat conversation" do?

Delete one Le Chat conversation by id (moves it to trash; Le Chat purges trashed conversations automatically after 30 days).

### How do I automatically delete Le Chat conversation on chat.mistral.ai?

Ask an AI agent connected to Reduck to run reduck/chat.mistral.ai/delete_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/delete_chat

### Is there a chat.mistral.ai API to delete Le Chat conversation?

You do not need one. "Delete Le Chat conversation" drives the real chat.mistral.ai pages in a browser, so it works whether or not chat.mistral.ai offers an API for this.

### What information do I need to provide?

Required: chatId.

### What does it return?

It returns title, chatId, status.

### Do I need to be logged in to chat.mistral.ai?

Yes. It acts as you on chat.mistral.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the chat.mistral.ai cookies saved by the Reduck extension.

### Does it change anything on chat.mistral.ai, or only read data?

It makes changes on chat.mistral.ai, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chat.mistral.ai/delete_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/delete_chat

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chat.mistral.ai/delete_chat
