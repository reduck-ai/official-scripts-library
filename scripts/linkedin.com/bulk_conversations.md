# Bulk-update LinkedIn conversations

Archive several classic LinkedIn messaging conversations at once, or mark them unread, the way the inbox does when you tick several conversations (not Sales Navigator). Pass the conversations' thread ids from linkedin.com/list_inbox and the action. The conversations are never opened, so they are not marked as read. Returns the action and the thread ids it was applied to. For one conversation, or to bring an archived conversation back to the inbox, use linkedin.com/archive_conversation. An empty inbox, with no conversation to tick, fails with a clear message.

- Site: linkedin.com
- Address: `reduck/linkedin.com/bulk_conversations`
- Updated: 2026-10-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/bulk_conversations`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/bulk_conversations
```

## Input

- `action` (string, required): archive moves the conversations out of the inbox; mark_unread marks them as unread.
- `threadIds` (array, required): Thread ids of the conversations, the threadId field of linkedin.com/list_inbox (also the part after /messaging/thread/ in a thread URL).

## Output

- `action` (string, required)
- `threadIds` (array, required): The thread ids LinkedIn accepted the action for.
- `httpStatus` (integer, required)

## FAQ

### What does "Bulk-update LinkedIn conversations" do?

Archive several classic LinkedIn messaging conversations at once, or mark them unread, the way the inbox does when you tick several conversations (not Sales Navigator). Pass the conversations' thread ids from linkedin.com/list_inbox and the action. The conversations are never opened, so they are not marked as read. Returns the action and the thread ids it was applied to. For one conversation, or to bring an archived conversation back to the inbox, use linkedin.com/archive_conversation. An empty inbox, with no conversation to tick, fails with a clear message.

### What information do I need to provide?

Required: threadIds, action.

### What does it return?

It returns action, threadIds, httpStatus.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/bulk_conversations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/bulk_conversations

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/bulk_conversations
