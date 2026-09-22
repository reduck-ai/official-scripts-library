# Trash Gmail thread

Automatically trash Gmail thread on mail.google.com. Move a Gmail thread to the Bin by its hex threadId. Acts from the list view, scanning the first 4 All Mail pages (~200 newest threads), and confirms the row actually left All Mail rather than trusting a toast. Returns trashed, threadId, and the page it was found on.

- Site: mail.google.com
- Address: `reduck/mail.google.com/trash_email`
- Updated: 2026-09-07 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/trash_email`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/trash_email
```

## Input

- `threadId` (string, required): Hex legacy thread id (as returned by search_emails).
- `account` (string, optional): Google account email to act as (authuser=). Without it Gmail picks u/0, nondeterministic in a multi-account browser jar.

## Output

- `trashed` (boolean, required)
- `threadId` (string, required)
- `page` (integer, optional): Which All Mail page the thread was found on (1-based).

## FAQ

### What does "Trash Gmail thread" do?

Move a Gmail thread to the Bin by its hex threadId. Acts from the list view, scanning the first 4 All Mail pages (~200 newest threads), and confirms the row actually left All Mail rather than trusting a toast. Returns trashed, threadId, and the page it was found on.

### How do I automatically trash Gmail thread on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/trash_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/trash_email

### Is there a mail.google.com API to trash Gmail thread?

You do not need one. "Trash Gmail thread" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: threadId. Optional: account.

### What does it return?

It returns page, trashed, threadId.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/trash_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/trash_email

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/trash_email
