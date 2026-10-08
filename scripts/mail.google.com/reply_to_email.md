# Reply to Gmail thread

Automatically reply to Gmail thread on mail.google.com. Reply (or reply-all) inside an existing Gmail conversation, given its thread id or the conversation's link, so the reply stays in the same thread with the original subject and quoted history. Optionally add Cc recipients, attach one file, or schedule the reply for later. Returns whether it was sent or scheduled, the conversation id and subject, and for scheduled replies the time Gmail shows.

- Site: mail.google.com
- Address: `reduck/mail.google.com/reply_to_email`
- Updated: 2026-10-07 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/reply_to_email`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/reply_to_email
```

## Input

- `body` (string, required): Plain-text reply body (newlines preserved). Long bodies are fine.
- `cc` (any, optional): Optional Cc address(es) added to the reply. A single string or an array of strings.
- `sendAt` (string, optional): Optional. Schedule the reply instead of sending it now: a local date and time with no offset (e.g. 2026-10-09T09:00), read in the browser's time zone. Must be at least a few minutes ahead.
- `account` (string, optional): Google account email to act as. Without it Gmail picks the first signed-in account, which may not be the one you expect if several accounts share the browser.
- `replyAll` (boolean, optional): Reply to all recipients instead of just the sender.
- `threadId` (string, optional): Hex thread id as returned by search_emails, e.g. "19f2817451c27480". Give this or threadUrl.
- `threadUrl` (string, optional): The Gmail address of the conversation, as copied from the browser (e.g. https://mail.google.com/mail/u/0/#inbox/FMfcgz...). Give this or threadId.
- `attachment` (string, optional): Optional file to attach. From an agent: files: { attachment: { relativePath: "invoice.pdf" } }, a name inside the reduck folder on the Desktop. From the CLI: file:attachment=/path/to/file.
- `attachmentName` (string, optional): Filename the recipient sees, with its extension. Defaults to the file's own name.

## Output

- `sent` (boolean, required): True when the reply went out now. False when it was scheduled instead.
- `replyAll` (boolean, required)
- `threadId` (string, required): Hex id of the conversation the reply was added to.
- `cc` (array, optional)
- `subject` (string | null, optional): Subject of the conversation the reply joined.
- `scheduled` (boolean, optional)
- `attachment` (string, optional)
- `scheduledFor` (string | null, optional): The send date and time as Gmail shows it on the Scheduled list, in the account's language.
- `foundInScheduled` (boolean, optional)

## FAQ

### What does "Reply to Gmail thread" do?

Reply (or reply-all) inside an existing Gmail conversation, given its thread id or the conversation's link, so the reply stays in the same thread with the original subject and quoted history. Optionally add Cc recipients, attach one file, or schedule the reply for later. Returns whether it was sent or scheduled, the conversation id and subject, and for scheduled replies the time Gmail shows.

### How do I automatically reply to Gmail thread on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/reply_to_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/reply_to_email

### Is there a mail.google.com API to reply to Gmail thread?

You do not need one. "Reply to Gmail thread" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: body. Optional: cc, sendAt, account, replyAll, threadId, threadUrl, attachment, attachmentName.

### What does it return?

It returns cc, sent, subject, replyAll, threadId, scheduled, attachment, scheduledFor, foundInScheduled.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/reply_to_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/reply_to_email

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/reply_to_email
