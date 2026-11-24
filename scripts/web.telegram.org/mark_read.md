# Mark a Telegram conversation read or unread

Automatically mark a Telegram conversation read or unread on web.telegram.org. Mark a Telegram conversation as read, or as unread again with unread: true, without opening it. Returns the state after the run, read back from the chat list, and whether anything changed: asking for the state it already has changes nothing. The conversation must be among the ones the chat list shows first. Use it after reading a conversation with get_conversation, which does not mark it read.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/mark_read`
- Updated: 2026-11-23 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/mark_read`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/mark_read
```

## Input

- `peerId` (string, required): The conversation, as web.telegram.org/get_inbox returns it. It must be among the conversations the chat list shows first: this never opens the conversation, which would mark it read by itself.
- `unread` (boolean, optional): false to mark the conversation read; true to mark it unread again.

## Output

- `peerId` (string, required)
- `changed` (boolean, required): False when it was already in the asked state, and nothing was clicked.
- `unreadNow` (boolean, required): The conversation's state after the run, read back from the chat list.
- `account_used` (string | null, required)
- `accountId` (string, optional)
- `chatTitle` (string | null, optional)

## FAQ

### What does "Mark a Telegram conversation read or unread" do?

Mark a Telegram conversation as read, or as unread again with unread: true, without opening it. Returns the state after the run, read back from the chat list, and whether anything changed: asking for the state it already has changes nothing. The conversation must be among the ones the chat list shows first. Use it after reading a conversation with get_conversation, which does not mark it read.

### How do I automatically mark a Telegram conversation read or unread on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/mark_read, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/mark_read

### Is there a web.telegram.org API to mark a Telegram conversation read or unread?

You do not need one. "Mark a Telegram conversation read or unread" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Required: peerId. Optional: unread.

### What does it return?

It returns peerId, changed, accountId, chatTitle, unreadNow, account_used.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It makes changes on web.telegram.org, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/mark_read, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/mark_read

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/mark_read
