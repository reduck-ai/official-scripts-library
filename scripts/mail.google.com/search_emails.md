# Search Gmail

Automatically search Gmail on mail.google.com. Search the signed-in Gmail with the native query syntax (from:, to:, subject:, has:attachment, after:/before:, labels…) and return matching threads: threadId (feed it to get_thread / reply_to_email), sender, senderEmail, subject, snippet, date, unread, starred, hasAttachment. Results are threads rather than individual messages, which is Gmail's own search granularity, and only the first page of results is returned (up to 50).

- Site: mail.google.com
- Address: `reduck/mail.google.com/search_emails`
- Updated: 2026-09-14 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/search_emails`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/search_emails
```

## Input

- `query` (string, required): Gmail search query; full native operator syntax (from:, subject:, has:attachment, after:...).
- `limit` (integer, optional): Max rows to return (1-50, default 20).
- `account` (string, optional): Gmail account address to act as (authuser pin). Omit for u/0.

## Output

- `n` (integer, required)
- `query` (string, required)
- `emails` (array, required)

## FAQ

### What does "Search Gmail" do?

Search the signed-in Gmail with the native query syntax (from:, to:, subject:, has:attachment, after:/before:, labels…) and return matching threads: threadId (feed it to get_thread / reply_to_email), sender, senderEmail, subject, snippet, date, unread, starred, hasAttachment. Results are threads rather than individual messages, which is Gmail's own search granularity, and only the first page of results is returned (up to 50).

### How do I automatically search Gmail on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/search_emails, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/search_emails

### Is there a mail.google.com API to search Gmail?

You do not need one. "Search Gmail" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: limit, account.

### What does it return?

It returns n, query, emails.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It only reads. It looks things up on mail.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/search_emails, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/search_emails

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/search_emails
