# Mark Gmail thread as unread

Automatically mark Gmail thread as unread on mail.google.com. Mark a Gmail thread as unread by its hex threadId. Returns unread, threadId, the All Mail page it was found on, and already_unread. Acts from the All Mail list, scanning the first 4 pages (~200 newest threads). Safe to repeat: a thread that is already unread returns already_unread:true without clicking anything. Waits for Gmail to persist the change rather than returning on the optimistic row restyling, so the mail really is unread once the run ends.

- Site: mail.google.com
- Address: `reduck/mail.google.com/mark_unread`
- Updated: 2026-09-07 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/mark_unread`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/mark_unread
```

## Input

- `threadId` (string, required): Hex thread id, as returned by list_inbox / search_emails.
- `account` (string, optional): Gmail account address to act as (authuser pin). Omit for u/0.

## Output

- `page` (integer, required)
- `unread` (boolean, required)
- `threadId` (string, required)
- `already_unread` (boolean, optional)

## FAQ

### What does "Mark Gmail thread as unread" do?

Mark a Gmail thread as unread by its hex threadId. Returns unread, threadId, the All Mail page it was found on, and already_unread. Acts from the All Mail list, scanning the first 4 pages (~200 newest threads). Safe to repeat: a thread that is already unread returns already_unread:true without clicking anything. Waits for Gmail to persist the change rather than returning on the optimistic row restyling, so the mail really is unread once the run ends.

### How do I automatically mark Gmail thread as unread on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/mark_unread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/mark_unread

### Is there a mail.google.com API to mark Gmail thread as unread?

You do not need one. "Mark Gmail thread as unread" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: threadId. Optional: account.

### What does it return?

It returns page, unread, threadId, already_unread.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/mark_unread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/mark_unread

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/mark_unread
