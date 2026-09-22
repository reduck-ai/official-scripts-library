# Get Claude chat messages

Automatically get Claude chat messages on claude.ai. Full message transcript of one Claude.ai conversation by uuid, oldest→newest. `text` is the readable prose; `tools` lists tool calls the UI renders as cards.

- Site: claude.ai
- Address: `reduck/claude.ai/get_chat_messages`
- Updated: 2026-07-20 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/get_chat_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/get_chat_messages
```

## Input

- `conversation_uuid` (string, required): The conversation uuid, as returned by list_chats / search_chats (also the /chat/<uuid> URL segment).

## Output

- `name` (string, required)
- `uuid` (string, required)
- `messages` (array, required)
- `model` (string | null, optional)
- `created_at` (string, optional)
- `is_starred` (boolean | null, optional)
- `updated_at` (string, optional)

## FAQ

### What does "Get Claude chat messages" do?

Full message transcript of one Claude.ai conversation by uuid, oldest→newest. `text` is the readable prose; `tools` lists tool calls the UI renders as cards.

### How do I automatically get Claude chat messages on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/get_chat_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/get_chat_messages

### Is there a claude.ai API to get Claude chat messages?

You do not need one. "Get Claude chat messages" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Required: conversation_uuid.

### What does it return?

It returns name, uuid, model, messages, created_at, is_starred, updated_at.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

Unknown: its author has not declared whether it changes anything on claude.ai, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/get_chat_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/get_chat_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/get_chat_messages
