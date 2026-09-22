# Reply to Gmail thread

Automatically reply to Gmail thread on mail.google.com. Reply (or reply-all) in a Gmail thread by its hex threadId (as returned by search_emails), with a plain-text body. Replies to the latest message of the thread. Returns sent, threadId, replyAll.

- Site: mail.google.com
- Address: `reduck/mail.google.com/reply_to_email`
- Updated: 2026-09-17 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/reply_to_email`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/reply_to_email
```

## Input

- `body` (string, required): Plain-text reply body (newlines preserved).
- `threadId` (string, required): Hex legacy thread id, e.g. "19f2817451c27480".
- `account` (string, optional): Google account email to act as (authuser=). Without it Gmail picks u/0, which is NOT deterministic when several accounts share the browser's cookie jar.
- `replyAll` (boolean, optional): Reply to all recipients instead of just the sender.

## Output

- `sent` (boolean, required)
- `replyAll` (boolean, required)
- `threadId` (string, required)

## FAQ

### What does "Reply to Gmail thread" do?

Reply (or reply-all) in a Gmail thread by its hex threadId (as returned by search_emails), with a plain-text body. Replies to the latest message of the thread. Returns sent, threadId, replyAll.

### How do I automatically reply to Gmail thread on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/reply_to_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/reply_to_email

### Is there a mail.google.com API to reply to Gmail thread?

You do not need one. "Reply to Gmail thread" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: threadId, body. Optional: account, replyAll.

### What does it return?

It returns sent, replyAll, threadId.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/reply_to_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/reply_to_email

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/reply_to_email
