# Reply to Gmail thread

Automatically reply to Gmail thread on mail.google.com. Reply (or reply-all) inside an existing Gmail conversation, given its thread id or the conversation's link, so the reply stays in the same thread with the original subject and quoted history. Optionally add Cc recipients, attach up to 10 files (attachment, attachment2 ... attachment10; name them with attachmentNames), or schedule the reply for later. Returns whether it was sent or scheduled, the conversation id and subject, every attachment's name, and for scheduled replies the time Gmail shows. To start a new conversation instead, use mail.google.com/send_email.

- Site: mail.google.com
- Address: `reduck/mail.google.com/reply_to_email`
- Updated: 2026-11-10 (v14)
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
- `attachment` (string, optional): Optional file to attach (the first one). From an agent: files: { attachment: { relativePath: "invoice.pdf" } }, a name inside the reduck folder on the Desktop. From the CLI: file:attachment=/path/to/file. For more files in the same reply, also pass attachment2, attachment3, ... up to attachment10.
- `attachment2` (string, optional): Optional second file, sent with the others in the same reply. Pass it the same way as attachment.
- `attachment3` (string, optional): Optional third file.
- `attachment4` (string, optional): Optional fourth file.
- `attachment5` (string, optional): Optional fifth file.
- `attachment6` (string, optional): Optional sixth file.
- `attachment7` (string, optional): Optional seventh file.
- `attachment8` (string, optional): Optional eighth file.
- `attachment9` (string, optional): Optional ninth file.
- `attachment10` (string, optional): Optional tenth file.
- `attachmentName` (string, optional): Filename the recipient sees for the first attachment, with its extension. Defaults to the file's own name. For several files use attachmentNames instead.
- `attachmentNames` (array, optional): Filenames the recipient sees, one per attached file, in order (attachment, attachment2, ...). Needed when sending several files as bytes, which otherwise arrive named after their input.

## Output

- `sent` (boolean, required): True when the reply went out now. False when it was scheduled instead.
- `replyAll` (boolean, required)
- `threadId` (string, required): Hex id of the conversation the reply was added to.
- `cc` (array, optional)
- `subject` (string | null, optional): Subject of the conversation the reply joined.
- `scheduled` (boolean, optional)
- `attachment` (string, optional): The filename the first attachment was sent under.
- `attachments` (array, optional): Every attachment's filename, in order, as Gmail showed it before sending.
- `scheduledFor` (string | null, optional): The send date and time as Gmail shows it on the Scheduled list, in the account's language.
- `foundInScheduled` (boolean, optional)

## FAQ

### What does "Reply to Gmail thread" do?

Reply (or reply-all) inside an existing Gmail conversation, given its thread id or the conversation's link, so the reply stays in the same thread with the original subject and quoted history. Optionally add Cc recipients, attach up to 10 files (attachment, attachment2 ... attachment10; name them with attachmentNames), or schedule the reply for later. Returns whether it was sent or scheduled, the conversation id and subject, every attachment's name, and for scheduled replies the time Gmail shows. To start a new conversation instead, use mail.google.com/send_email.

### How do I automatically reply to Gmail thread on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/reply_to_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/reply_to_email

### Is there a mail.google.com API to reply to Gmail thread?

You do not need one. "Reply to Gmail thread" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: body. Optional: cc, sendAt, account, replyAll, threadId, threadUrl, attachment, attachment2, attachment3, attachment4, attachment5, attachment6, attachment7, attachment8, attachment9, attachment10, attachmentName, attachmentNames.

### What does it return?

It returns cc, sent, subject, replyAll, threadId, scheduled, attachment, attachments, scheduledFor, foundInScheduled.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/reply_to_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/reply_to_email

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/reply_to_email
