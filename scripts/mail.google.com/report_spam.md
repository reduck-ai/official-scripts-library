# Report Gmail thread as spam

Automatically report Gmail thread as spam on mail.google.com. Report a Gmail thread as spam by its hex threadId (moves it to Spam). Requires an authenticated mail.google.com session. Works from the All Mail list view, scanning the first 4 pages (~200 newest threads), and is locale-independent. Returns reportedSpam, threadId, and the page it was found on.

- Site: mail.google.com
- Address: `reduck/mail.google.com/report_spam`
- Updated: 2026-09-07 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/report_spam`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/report_spam
```

## Input

- `threadId` (string, required): Hex thread id, as returned by list_inbox / search_emails.
- `account` (string, optional): Gmail account address to act as (authuser pin). Omit for u/0.

## Output

- `page` (integer, required)
- `threadId` (string, required)
- `reportedSpam` (boolean, required)

## FAQ

### What does "Report Gmail thread as spam" do?

Report a Gmail thread as spam by its hex threadId (moves it to Spam). Requires an authenticated mail.google.com session. Works from the All Mail list view, scanning the first 4 pages (~200 newest threads), and is locale-independent. Returns reportedSpam, threadId, and the page it was found on.

### How do I automatically report Gmail thread as spam on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/report_spam, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/report_spam

### Is there a mail.google.com API to report Gmail thread as spam?

You do not need one. "Report Gmail thread as spam" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: threadId. Optional: account.

### What does it return?

It returns page, threadId, reportedSpam.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/report_spam, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/report_spam

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/report_spam
