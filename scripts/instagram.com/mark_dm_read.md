# Mark an Instagram DM thread as read

Automatically mark an Instagram DM thread as read on instagram.com. Mark an Instagram DM conversation as read by opening it, by the conversation partner's username. Instagram has no separate "mark as read" button — opening a conversation is what clears its unread state — so this opens it and confirms the unread flag actually cleared. Idempotent — reports if the thread is already read instead of reopening it.

- Site: instagram.com
- Address: `reduck/instagram.com/mark_dm_read`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/mark_dm_read`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/mark_dm_read
```

## Input

- `username` (string, required): Handle of the conversation partner, without @.

## Output

- `status` (string, required)
- `username` (string, required)
- `threadId` (string | null, optional)

## FAQ

### What does "Mark an Instagram DM thread as read" do?

Mark an Instagram DM conversation as read by opening it, by the conversation partner's username. Instagram has no separate "mark as read" button — opening a conversation is what clears its unread state — so this opens it and confirms the unread flag actually cleared. Idempotent — reports if the thread is already read instead of reopening it.

### How do I automatically mark an Instagram DM thread as read on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/mark_dm_read, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/mark_dm_read

### Is there a instagram.com API to mark an Instagram DM thread as read?

You do not need one. "Mark an Instagram DM thread as read" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns status, threadId, username.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/mark_dm_read, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/mark_dm_read

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/mark_dm_read
