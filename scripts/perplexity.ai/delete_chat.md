# Delete Perplexity chat

Automatically delete Perplexity chat on perplexity.ai. Permanently delete one Perplexity thread from your recent history, by the chatId returned from list_chats.

- Site: perplexity.ai
- Address: `reduck/perplexity.ai/delete_chat`
- Updated: 2026-08-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/perplexity.ai/delete_chat`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/delete_chat
```

## Input

- `chatId` (string, required): Thread id from list_chats (the id in its /search/<id> URL). Must be one of the account's recent threads shown in the sidebar.

## Output

- `chatId` (string, required): The thread id that was deleted, echoed back.
- `deleted` (boolean, required): True once Perplexity's own delete request has answered successfully. The script fails rather than returning false, so a returned record always means the thread is gone.

## FAQ

### What does "Delete Perplexity chat" do?

Permanently delete one Perplexity thread from your recent history, by the chatId returned from list_chats.

### How do I automatically delete Perplexity chat on perplexity.ai?

Ask an AI agent connected to Reduck to run reduck/perplexity.ai/delete_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/delete_chat

### Is there a perplexity.ai API to delete Perplexity chat?

You do not need one. "Delete Perplexity chat" drives the real perplexity.ai pages in a browser, so it works whether or not perplexity.ai offers an API for this.

### What information do I need to provide?

Required: chatId.

### What does it return?

It returns chatId, deleted.

### Do I need to be logged in to perplexity.ai?

Yes. It acts as you on perplexity.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the perplexity.ai cookies saved by the Reduck extension.

### Does it change anything on perplexity.ai, or only read data?

It makes changes on perplexity.ai, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/perplexity.ai/delete_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/delete_chat

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/perplexity.ai/delete_chat
