# Sales Navigator – Get conversation thread

Automatically get conversation thread on linkedin.com. Fetch a full LinkedIn Sales Navigator conversation thread by its threadId (from get_inbox), pulling up to messageCount messages. Returns the counterpart participant(s), totalMessageCount, whether it was truncated, and every message in chronological order (oldest first) with body, subject (for InMails), whether it is a regular message or an InMail, deliveredAt, lastEditedAt, attachments, and direction (sent/received). A 1:1 thread has one counterpart, group threads list all; if returnedCount is below totalMessageCount, raise messageCount. Needs a Sales Navigator seat.

- Site: linkedin.com
- Address: `reduck/linkedin.com/sales_navigator_get_thread`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/sales_navigator_get_thread`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_get_thread
```

## Input

- `threadId` (string, required): Conversation thread id from get_inbox (e.g. '2-NWU3...XzEwMA==').
- `messageCount` (integer, optional): Max messages to fetch. Default 100 — enough for the whole thread in most cases. Compare returnedCount to totalMessageCount to detect truncation and raise this.

## Output

- `messages` (array, required): Chronological, oldest first.
- `threadId` (string, required)
- `archived` (boolean | null, optional)
- `truncated` (boolean, optional): true when returnedCount < totalMessageCount — raise messageCount.
- `viewerUrn` (string | null, optional)
- `viewerName` (string | null, optional)
- `unreadCount` (integer | null, optional)
- `participants` (array, optional): Counterpart(s) — everyone except the viewer.
- `returnedCount` (integer, optional)
- `totalMessageCount` (integer | null, optional)

## FAQ

### What does "Sales Navigator – Get conversation thread" do?

Fetch a full LinkedIn Sales Navigator conversation thread by its threadId (from get_inbox), pulling up to messageCount messages. Returns the counterpart participant(s), totalMessageCount, whether it was truncated, and every message in chronological order (oldest first) with body, subject (for InMails), whether it is a regular message or an InMail, deliveredAt, lastEditedAt, attachments, and direction (sent/received). A 1:1 thread has one counterpart, group threads list all; if returnedCount is below totalMessageCount, raise messageCount. Needs a Sales Navigator seat.

### How do I automatically get conversation thread on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_get_thread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_get_thread

### Is there a linkedin.com API to get conversation thread?

You do not need one. "Sales Navigator – Get conversation thread" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: threadId. Optional: messageCount.

### What does it return?

It returns archived, messages, threadId, truncated, viewerUrn, viewerName, unreadCount, participants, returnedCount, totalMessageCount.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

Unknown: its author has not declared whether it changes anything on linkedin.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_get_thread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_get_thread

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/sales_navigator_get_thread
