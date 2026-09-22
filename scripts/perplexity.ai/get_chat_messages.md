# Get Perplexity chat messages

Automatically get Perplexity chat messages on perplexity.ai. Full message transcript of one Perplexity thread, by the chatId returned from list_chats.

- Site: perplexity.ai
- Address: `reduck/perplexity.ai/get_chat_messages`
- Updated: 2026-08-25 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/perplexity.ai/get_chat_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/get_chat_messages
```

## Input

- `chatId` (string, required): Thread id from list_chats (the id in its /search/<id> URL).

## Output

- `title` (string, required)
- `chatId` (string, required)
- `messages` (array, required)

## FAQ

### What does "Get Perplexity chat messages" do?

Full message transcript of one Perplexity thread, by the chatId returned from list_chats.

### How do I automatically get Perplexity chat messages on perplexity.ai?

Ask an AI agent connected to Reduck to run reduck/perplexity.ai/get_chat_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/get_chat_messages

### Is there a perplexity.ai API to get Perplexity chat messages?

You do not need one. "Get Perplexity chat messages" drives the real perplexity.ai pages in a browser, so it works whether or not perplexity.ai offers an API for this.

### What information do I need to provide?

Required: chatId.

### What does it return?

It returns title, chatId, messages.

### Do I need to be logged in to perplexity.ai?

Yes. It acts as you on perplexity.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the perplexity.ai cookies saved by the Reduck extension.

### Does it change anything on perplexity.ai, or only read data?

It only reads. It looks things up on perplexity.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/perplexity.ai/get_chat_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/get_chat_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/perplexity.ai/get_chat_messages
