# Forward Gmail thread

Automatically forward Gmail thread on mail.google.com. Forward an entire Gmail thread to one recipient, with an optional leading note. Takes the hex threadId that search_emails returns, and forwards the whole conversation inline rather than a single message. Returns forwarded, threadId and to. The thread must be on the first page of All Mail, newest-first, so older conversations cannot be reached this way.

- Site: mail.google.com
- Address: `reduck/mail.google.com/forward_email`
- Updated: 2026-09-17 (v21)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/forward_email`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/forward_email
```

## Input

- `to` (string, required): Recipient email address.
- `threadId` (string, required): Hex legacy thread id.
- `note` (string, optional): Optional plain-text note prepended above the forwarded content.
- `account` (string, optional): Google account email to act as (authuser=). Without it Gmail picks u/0, nondeterministic in a multi-account browser jar.

## Output

- `to` (string, required)
- `threadId` (string, required)
- `forwarded` (boolean, required)

## FAQ

### What does "Forward Gmail thread" do?

Forward an entire Gmail thread to one recipient, with an optional leading note. Takes the hex threadId that search_emails returns, and forwards the whole conversation inline rather than a single message. Returns forwarded, threadId and to. The thread must be on the first page of All Mail, newest-first, so older conversations cannot be reached this way.

### How do I automatically forward Gmail thread on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/forward_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/forward_email

### Is there a mail.google.com API to forward Gmail thread?

You do not need one. "Forward Gmail thread" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: threadId, to. Optional: note, account.

### What does it return?

It returns to, threadId, forwarded.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/forward_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/forward_email

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/forward_email
