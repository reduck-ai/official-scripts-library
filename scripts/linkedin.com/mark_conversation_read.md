# Mark LinkedIn conversation as read

Automatically mark LinkedIn conversation as read on linkedin.com. Mark a classic LinkedIn messaging conversation (NOT Sales Navigator) as read, by thread URL from list_inbox. Counterpart to mark_conversation_unread. Opening the thread is itself what marks it read, so this always returns status "read" — it can't tell you whether the conversation was already read beforehand; check list_inbox's unreadCount first if you need that.

- Site: linkedin.com
- Address: `reduck/linkedin.com/mark_conversation_read`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/mark_conversation_read`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/mark_conversation_read
```

## Input

- `threadUrl` (string, required): URL of the conversation thread, e.g. https://www.linkedin.com/messaging/thread/<id>/ (from list_inbox)

## Output

- `status` (string, required): read = the conversation is read once this returns
- `threadUrl` (string, required)
- `seenMutationObserved` (boolean, optional): Diagnostic only: whether the seen/read mutation was seen on this load. Not a prior-state signal — it fires on essentially every load.

## FAQ

### What does "Mark LinkedIn conversation as read" do?

Mark a classic LinkedIn messaging conversation (NOT Sales Navigator) as read, by thread URL from list_inbox. Counterpart to mark_conversation_unread. Opening the thread is itself what marks it read, so this always returns status "read" — it can't tell you whether the conversation was already read beforehand; check list_inbox's unreadCount first if you need that.

### How do I automatically mark LinkedIn conversation as read on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/mark_conversation_read, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/mark_conversation_read

### Is there a linkedin.com API to mark LinkedIn conversation as read?

You do not need one. "Mark LinkedIn conversation as read" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: threadUrl.

### What does it return?

It returns status, threadUrl, seenMutationObserved.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/mark_conversation_read, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/mark_conversation_read

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/mark_conversation_read
