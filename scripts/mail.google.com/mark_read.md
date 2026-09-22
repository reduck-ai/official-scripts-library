# Mark Gmail thread as read

Automatically mark Gmail thread as read on mail.google.com. Mark a Gmail thread as read by its hex threadId. Returns read, threadId, the All Mail page it was found on, and already_read. Acts from the All Mail list, scanning the first 4 pages (~200 newest threads). Safe to repeat: a thread that is already read returns already_read:true without clicking anything. Waits for Gmail to persist the change rather than returning on the optimistic row restyling, so the mail really is read once the run ends.

- Site: mail.google.com
- Address: `reduck/mail.google.com/mark_read`
- Updated: 2026-09-07 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/mark_read`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/mark_read
```

## Input

- `threadId` (string, required): Hex legacy thread id (as returned by search_emails).
- `account` (string, optional): Google account email to act as (authuser=). Without it Gmail picks u/0, nondeterministic in a multi-account browser jar.

## Output

- `read` (boolean, required)
- `threadId` (string, required)
- `page` (integer, optional): Which All Mail page the thread was found on (1-based).
- `already_read` (boolean, optional): true = the thread was already read; nothing was clicked.

## FAQ

### What does "Mark Gmail thread as read" do?

Mark a Gmail thread as read by its hex threadId. Returns read, threadId, the All Mail page it was found on, and already_read. Acts from the All Mail list, scanning the first 4 pages (~200 newest threads). Safe to repeat: a thread that is already read returns already_read:true without clicking anything. Waits for Gmail to persist the change rather than returning on the optimistic row restyling, so the mail really is read once the run ends.

### How do I automatically mark Gmail thread as read on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/mark_read, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/mark_read

### Is there a mail.google.com API to mark Gmail thread as read?

You do not need one. "Mark Gmail thread as read" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: threadId. Optional: account.

### What does it return?

It returns page, read, threadId, already_read.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/mark_read, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/mark_read

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/mark_read
