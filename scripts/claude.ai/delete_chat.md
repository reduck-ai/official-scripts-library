# Delete Claude chats

Automatically delete Claude chats on claude.ai. Permanently delete one or more Claude.ai conversations by uuid (from list_chats, search_chats, or ask's conversationId). This is irreversible and cannot be undone — claude.ai has no trash and no undo for conversations. dryRun (default true) resolves every uuid and reports the exact conversation names that would be deleted, without deleting anything; set it to false to actually delete. Each uuid is resolved before the destructive call, so a wrong or already-deleted uuid is reported as notFound rather than acted on blindly, and each deletion is confirmed by re-reading the conversation until the site itself 404s it — never on the strength of an optimistic 204. Addresses conversations by uuid, not by title: titles are model-generated and routinely collide.

- Site: claude.ai
- Address: `reduck/claude.ai/delete_chat`
- Updated: 2026-08-17 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/delete_chat`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/delete_chat
```

## Input

- `uuids` (array, required): Conversation uuids to delete. Order is preserved in the results.
- `dryRun` (boolean, optional): If true (default), resolve every uuid and report what WOULD be deleted, deleting nothing. Set false to actually delete.

## Output

- `dryRun` (boolean, required): Echoes the mode this run actually ran in — false means conversations were really deleted.
- `results` (array, required): One entry per requested uuid, in the order passed.

## FAQ

### What does "Delete Claude chats" do?

Permanently delete one or more Claude.ai conversations by uuid (from list_chats, search_chats, or ask's conversationId). This is irreversible and cannot be undone — claude.ai has no trash and no undo for conversations. dryRun (default true) resolves every uuid and reports the exact conversation names that would be deleted, without deleting anything; set it to false to actually delete. Each uuid is resolved before the destructive call, so a wrong or already-deleted uuid is reported as notFound rather than acted on blindly, and each deletion is confirmed by re-reading the conversation until the site itself 404s it — never on the strength of an optimistic 204. Addresses conversations by uuid, not by title: titles are model-generated and routinely collide.

### How do I automatically delete Claude chats on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/delete_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/delete_chat

### Is there a claude.ai API to delete Claude chats?

You do not need one. "Delete Claude chats" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Required: uuids. Optional: dryRun.

### What does it return?

It returns dryRun, results.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It makes changes on claude.ai, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/delete_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/delete_chat

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/delete_chat
