# Get Le Chat conversation messages

Automatically get Le Chat conversation messages on chat.mistral.ai. Full message transcript of one Le Chat conversation by id, oldest to newest.

- Site: chat.mistral.ai
- Address: `reduck/chat.mistral.ai/get_chat_messages`
- Updated: 2026-08-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chat.mistral.ai/get_chat_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/get_chat_messages
```

## Input

- `chatId` (string, required): Conversation id, from list_chats or search_chats

## Output

- `chatId` (string, required)
- `messages` (array, required)

## FAQ

### What does "Get Le Chat conversation messages" do?

Full message transcript of one Le Chat conversation by id, oldest to newest.

### How do I automatically get Le Chat conversation messages on chat.mistral.ai?

Ask an AI agent connected to Reduck to run reduck/chat.mistral.ai/get_chat_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/get_chat_messages

### Is there a chat.mistral.ai API to get Le Chat conversation messages?

You do not need one. "Get Le Chat conversation messages" drives the real chat.mistral.ai pages in a browser, so it works whether or not chat.mistral.ai offers an API for this.

### What information do I need to provide?

Required: chatId.

### What does it return?

It returns chatId, messages.

### Do I need to be logged in to chat.mistral.ai?

Yes. It acts as you on chat.mistral.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the chat.mistral.ai cookies saved by the Reduck extension.

### Does it change anything on chat.mistral.ai, or only read data?

It only reads. It looks things up on chat.mistral.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chat.mistral.ai/get_chat_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/get_chat_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chat.mistral.ai/get_chat_messages
