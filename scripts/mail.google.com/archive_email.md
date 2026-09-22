# Archive Gmail thread

Automatically archive Gmail thread on mail.google.com. Archive a Gmail thread by its hex threadId (removes it from the Inbox; it stays in All Mail). Returns archived, threadId, and the Inbox page it was found on.

- Site: mail.google.com
- Address: `reduck/mail.google.com/archive_email`
- Updated: 2026-09-07 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/archive_email`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/archive_email
```

## Input

- `threadId` (string, required): Hex legacy thread id (as returned by search_emails).
- `account` (string, optional): Google account email to act as (authuser=). Without it Gmail picks u/0, nondeterministic in a multi-account browser jar.

## Output

- `archived` (boolean, required)
- `threadId` (string, required)
- `page` (integer | null, optional): Which Inbox page the thread was found on (1-based), or null when it was located through search instead.
- `already_archived` (boolean, optional): true = the thread was already out of the Inbox; nothing was clicked.

## FAQ

### What does "Archive Gmail thread" do?

Archive a Gmail thread by its hex threadId (removes it from the Inbox; it stays in All Mail). Returns archived, threadId, and the Inbox page it was found on.

### How do I automatically archive Gmail thread on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/archive_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/archive_email

### Is there a mail.google.com API to archive Gmail thread?

You do not need one. "Archive Gmail thread" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: threadId. Optional: account.

### What does it return?

It returns page, archived, threadId, already_archived.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/archive_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/archive_email

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/archive_email
