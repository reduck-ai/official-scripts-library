# Mark LinkedIn conversation as unread

Automatically mark LinkedIn conversation as unread on linkedin.com. Mark a classic LinkedIn messaging conversation (NOT Sales Navigator) as unread, by thread URL from list_inbox. On group conversations (3+ participants), this occasionally times out on a rare page-loading delay on LinkedIn's side — retry the call if that happens.

- Site: linkedin.com
- Address: `reduck/linkedin.com/mark_conversation_unread`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/mark_conversation_unread`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/mark_conversation_unread
```

## Input

- `threadUrl` (string, required): URL of the conversation thread, e.g. https://www.linkedin.com/messaging/thread/<id>/ (from list_inbox)

## Output

- `status` (string, required)
- `threadUrl` (string, required)

## FAQ

### What does "Mark LinkedIn conversation as unread" do?

Mark a classic LinkedIn messaging conversation (NOT Sales Navigator) as unread, by thread URL from list_inbox. On group conversations (3+ participants), this occasionally times out on a rare page-loading delay on LinkedIn's side — retry the call if that happens.

### How do I automatically mark LinkedIn conversation as unread on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/mark_conversation_unread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/mark_conversation_unread

### Is there a linkedin.com API to mark LinkedIn conversation as unread?

You do not need one. "Mark LinkedIn conversation as unread" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: threadUrl.

### What does it return?

It returns status, threadUrl.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/mark_conversation_unread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/mark_conversation_unread

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/mark_conversation_unread
