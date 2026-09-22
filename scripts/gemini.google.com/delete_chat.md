# Delete Gemini chat

Automatically delete Gemini chat on gemini.google.com. Permanently delete one Gemini conversation by id, via the conversation's own "Delete" menu.

- Site: gemini.google.com
- Address: `reduck/gemini.google.com/delete_chat`
- Updated: 2026-08-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gemini.google.com/delete_chat`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/delete_chat
```

## Input

- `conversation_id` (string, required): Conversation id to delete, as returned by list_chats/search_chats (also the /app/<id> URL segment). Irreversible: this deletes prompts, responses, and any content the chat created.

## Output

- `deleted` (boolean, required)
- `conversationId` (string, required)

## FAQ

### What does "Delete Gemini chat" do?

Permanently delete one Gemini conversation by id, via the conversation's own "Delete" menu.

### How do I automatically delete Gemini chat on gemini.google.com?

Ask an AI agent connected to Reduck to run reduck/gemini.google.com/delete_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/delete_chat

### Is there a gemini.google.com API to delete Gemini chat?

You do not need one. "Delete Gemini chat" drives the real gemini.google.com pages in a browser, so it works whether or not gemini.google.com offers an API for this.

### What information do I need to provide?

Required: conversation_id.

### What does it return?

It returns deleted, conversationId.

### Do I need to be logged in to gemini.google.com?

Yes. It acts as you on gemini.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the gemini.google.com cookies saved by the Reduck extension.

### Does it change anything on gemini.google.com, or only read data?

It makes changes on gemini.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gemini.google.com/delete_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/delete_chat

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/gemini.google.com/delete_chat
