# Delete Grok Chat

Automatically delete Grok Chat on grok.com. Permanently delete one Grok conversation by id. Deletion happens immediately when clicked — Grok shows a brief in-app "Undo" toast, but this script does not wait for or use it, so treat the deletion as irreversible once this returns.

- Site: grok.com
- Address: `reduck/grok.com/delete_chat`
- Updated: 2026-08-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/grok.com/delete_chat`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/grok.com/delete_chat
```

## Input

- `conversationId` (string, required): Grok conversation id to delete, from list_chats or a /c/<id> URL

## Output

- `deleted` (boolean, required)
- `conversationId` (string, required)

## FAQ

### What does "Delete Grok Chat" do?

Permanently delete one Grok conversation by id. Deletion happens immediately when clicked — Grok shows a brief in-app "Undo" toast, but this script does not wait for or use it, so treat the deletion as irreversible once this returns.

### How do I automatically delete Grok Chat on grok.com?

Ask an AI agent connected to Reduck to run reduck/grok.com/delete_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/grok.com/delete_chat

### Is there a grok.com API to delete Grok Chat?

You do not need one. "Delete Grok Chat" drives the real grok.com pages in a browser, so it works whether or not grok.com offers an API for this.

### What information do I need to provide?

Required: conversationId.

### What does it return?

It returns deleted, conversationId.

### Do I need to be logged in to grok.com?

Yes. It acts as you on grok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the grok.com cookies saved by the Reduck extension.

### Does it change anything on grok.com, or only read data?

It makes changes on grok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/grok.com/delete_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/grok.com/delete_chat

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/grok.com/delete_chat
