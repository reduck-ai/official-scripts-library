# Get Gmail thread

Automatically get Gmail thread on mail.google.com. Read a Gmail thread by its hex threadId (as returned by search_emails): subject plus every rendered message's from, fromEmail, to, date, plain-text body and attachment names.

- Site: mail.google.com
- Address: `reduck/mail.google.com/get_thread`
- Updated: 2026-08-28 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/get_thread`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/get_thread
```

## Input

- `threadId` (string, required): Hex legacy thread id, e.g. "19f2817451c27480". Must belong to the account being read — an id from another mailbox, or a deleted thread, is refused rather than waited out.
- `account` (string, optional): Google account email to act as (authuser=). Without it Gmail picks u/0, which is NOT deterministic when several accounts share the browser's cookie jar.

## Output

- `n` (number, required)
- `subject` (string | null, required)
- `messages` (array, required)
- `threadId` (string, required)

## FAQ

### What does "Get Gmail thread" do?

Read a Gmail thread by its hex threadId (as returned by search_emails): subject plus every rendered message's from, fromEmail, to, date, plain-text body and attachment names.

### How do I automatically get Gmail thread on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/get_thread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/get_thread

### Is there a mail.google.com API to get Gmail thread?

You do not need one. "Get Gmail thread" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: threadId. Optional: account.

### What does it return?

It returns n, subject, messages, threadId.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It only reads. It looks things up on mail.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/get_thread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/get_thread

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/get_thread
