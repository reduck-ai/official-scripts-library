# Get Gemini chat messages

Automatically get Gemini chat messages on gemini.google.com. Full message transcript of one Gemini conversation by id, oldest to newest.

- Site: gemini.google.com
- Address: `reduck/gemini.google.com/get_chat_messages`
- Updated: 2026-08-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gemini.google.com/get_chat_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/get_chat_messages
```

## Input

- `conversation_id` (string, required): Conversation id, as returned by list_chats/search_chats (also the /app/<id> URL segment).

## Output

- `messages` (array, required)
- `conversationId` (string, required)

## FAQ

### What does "Get Gemini chat messages" do?

Full message transcript of one Gemini conversation by id, oldest to newest.

### How do I automatically get Gemini chat messages on gemini.google.com?

Ask an AI agent connected to Reduck to run reduck/gemini.google.com/get_chat_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/get_chat_messages

### Is there a gemini.google.com API to get Gemini chat messages?

You do not need one. "Get Gemini chat messages" drives the real gemini.google.com pages in a browser, so it works whether or not gemini.google.com offers an API for this.

### What information do I need to provide?

Required: conversation_id.

### What does it return?

It returns messages, conversationId.

### Do I need to be logged in to gemini.google.com?

Yes. It acts as you on gemini.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the gemini.google.com cookies saved by the Reduck extension.

### Does it change anything on gemini.google.com, or only read data?

It only reads. It looks things up on gemini.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gemini.google.com/get_chat_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/get_chat_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/gemini.google.com/get_chat_messages
