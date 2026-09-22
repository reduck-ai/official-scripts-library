# Get Grok Chat Messages

Automatically get Grok Chat Messages on grok.com. Full message transcript of one Grok conversation by id, oldest to newest: each message's role (user/assistant), text, and any inline-cited sources on assistant messages.

- Site: grok.com
- Address: `reduck/grok.com/get_chat_messages`
- Updated: 2026-08-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/grok.com/get_chat_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/grok.com/get_chat_messages
```

## Input

- `conversationId` (string, required): Grok conversation id, from list_chats or a /c/<id> URL

## Output

- `messages` (array, required)

## FAQ

### What does "Get Grok Chat Messages" do?

Full message transcript of one Grok conversation by id, oldest to newest: each message's role (user/assistant), text, and any inline-cited sources on assistant messages.

### How do I automatically get Grok Chat Messages on grok.com?

Ask an AI agent connected to Reduck to run reduck/grok.com/get_chat_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/grok.com/get_chat_messages

### Is there a grok.com API to get Grok Chat Messages?

You do not need one. "Get Grok Chat Messages" drives the real grok.com pages in a browser, so it works whether or not grok.com offers an API for this.

### What information do I need to provide?

Required: conversationId.

### What does it return?

It returns messages.

### Do I need to be logged in to grok.com?

Yes. It acts as you on grok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the grok.com cookies saved by the Reduck extension.

### Does it change anything on grok.com, or only read data?

It only reads. It looks things up on grok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/grok.com/get_chat_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/grok.com/get_chat_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/grok.com/get_chat_messages
