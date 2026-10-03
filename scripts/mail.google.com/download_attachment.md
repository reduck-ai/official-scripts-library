# Download Gmail attachments

Automatically download Gmail attachments on mail.google.com. Download every attachment of a Gmail thread, given its thread id as returned by search_emails, and save the files to your computer under their real names. Returns the thread id, how many files were saved, and each file's name and path. Attachments from every message in the thread are included, and inline images count as attachments.

- Site: mail.google.com
- Address: `reduck/mail.google.com/download_attachment`
- Updated: 2026-10-02 (v15)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/download_attachment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/download_attachment
```

## Input

- `threadId` (string, required): Hex legacy thread id.
- `account` (string, optional): Google account email to act as (authuser=). Without it Gmail picks u/0, nondeterministic in a multi-account browser jar.

## Output

- `n` (number, required)
- `files` (array, required)
- `threadId` (string, required)

## FAQ

### What does "Download Gmail attachments" do?

Download every attachment of a Gmail thread, given its thread id as returned by search_emails, and save the files to your computer under their real names. Returns the thread id, how many files were saved, and each file's name and path. Attachments from every message in the thread are included, and inline images count as attachments.

### How do I automatically download Gmail attachments on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/download_attachment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/download_attachment

### Is there a mail.google.com API to download Gmail attachments?

You do not need one. "Download Gmail attachments" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: threadId. Optional: account.

### What does it return?

It returns n, files, threadId.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It only reads. It looks things up on mail.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/download_attachment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/download_attachment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/download_attachment
