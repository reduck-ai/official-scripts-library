# Send Gmail email

Automatically send Gmail email on mail.google.com. Send an email from the signed-in Gmail account, with a plain-text body and an optional single file attachment.

- Site: mail.google.com
- Address: `reduck/mail.google.com/send_email`
- Updated: 2026-09-21 (v23)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/send_email`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/send_email
```

## Input

- `to` (any, required): Recipient email address(es). A single string or an array of strings.
- `subject` (string, required): Email subject line.
- `cc` (any, optional): Optional Cc address(es). A single string or an array of strings.
- `bcc` (any, optional): Optional Bcc address(es). A single string or an array of strings.
- `body` (string, optional): Plain-text message body.
- `account` (string, optional): Google account email to send as. Without it, Gmail uses the first signed-in account, which may not be the one you expect if several accounts share the browser.
- `attachment` (string, optional): Optional file to attach. From an agent: files: { attachment: { relativePath: "invoice.pdf" } }, a name inside the reduck folder on the Desktop. From the CLI: file:attachment=/path/to/file. Omit it to send without an attachment.
- `attachmentName` (string, optional): Filename the recipient sees, with its extension (e.g. 'invoice.pdf'). Defaults to the file's own name, which a file named by relativePath keeps. Pass it when sending bytes from the CLI, where the file otherwise arrives named 'attachment'.

## Output

- `to` (array, required)
- `sent` (boolean, required)
- `subject` (string, required)
- `cc` (array, optional)
- `bcc` (array, optional)
- `attachment` (string, optional): The filename the attachment was sent under, when one was attached.

## FAQ

### What does "Send Gmail email" do?

Send an email from the signed-in Gmail account, with a plain-text body and an optional single file attachment.

### How do I automatically send Gmail email on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/send_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/send_email

### Is there a mail.google.com API to send Gmail email?

You do not need one. "Send Gmail email" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: to, subject. Optional: cc, bcc, body, account, attachment, attachmentName.

### What does it return?

It returns cc, to, bcc, sent, subject, attachment.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/send_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/send_email

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/send_email
