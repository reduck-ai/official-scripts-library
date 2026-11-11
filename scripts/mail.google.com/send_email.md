# Send Gmail email

Automatically send Gmail email on mail.google.com. Send an email from the signed-in Gmail account, with a plain-text body and up to 10 file attachments in the same email (attachment, attachment2 ... attachment10; name them with attachmentNames). Returns every attachment's name as Gmail showed it before sending. Always starts a new conversation. To answer inside an existing thread, use mail.google.com/reply_to_email.

- Site: mail.google.com
- Address: `reduck/mail.google.com/send_email`
- Updated: 2026-11-10 (v40)
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
- `sendAt` (string, optional): Optional. Schedule the email instead of sending it now: a local date and time with no offset (e.g. 2026-10-06T09:00), read in the browser's time zone. Must be at least a few minutes ahead. The email then waits in Gmail's Scheduled folder, where it can still be edited or cancelled.
- `account` (string, optional): Google account email to send as. Without it, Gmail uses the first signed-in account, which may not be the one you expect if several accounts share the browser.
- `attachment` (string, optional): Optional file to attach (the first one). From an agent: files: { attachment: { relativePath: "invoice.pdf" } }, a name inside the reduck folder on the Desktop. From the CLI: file:attachment=/path/to/file. Omit it to send without an attachment. For more files in the same email, also pass attachment2, attachment3, ... up to attachment10.
- `attachment2` (string, optional): Optional second file, sent with the others in the same email. Pass it the same way as attachment.
- `attachment3` (string, optional): Optional third file.
- `attachment4` (string, optional): Optional fourth file.
- `attachment5` (string, optional): Optional fifth file.
- `attachment6` (string, optional): Optional sixth file.
- `attachment7` (string, optional): Optional seventh file.
- `attachment8` (string, optional): Optional eighth file.
- `attachment9` (string, optional): Optional ninth file.
- `attachment10` (string, optional): Optional tenth file.
- `attachmentName` (string, optional): Filename the recipient sees for the first attachment, with its extension (e.g. 'invoice.pdf'). Defaults to the file's own name, which a file named by relativePath keeps. Pass it when sending bytes from the CLI, where the file otherwise arrives named after its input. For several files use attachmentNames instead.
- `attachmentNames` (array, optional): Filenames the recipient sees, one per attached file, in order (attachment, attachment2, ...). Needed when sending several files as bytes, which otherwise arrive named after their input.
- `confirmSharingWarning` (boolean, optional): Optional. When the body links a Drive file a recipient cannot open (typically a recipient without a Google account), Gmail asks about the file's access before sending. True sends anyway and never changes the file's sharing: when Gmail offers to open the file to anyone with the link, the script picks sending without updating access instead. Leave it off and such a question makes the script stop with an error naming it, nothing sent. Share the file yourself first if the recipients must be able to open it.

## Output

- `to` (array, required)
- `sent` (boolean, required): True when the email went out now. False when it was scheduled instead.
- `subject` (string, required)
- `cc` (array, optional)
- `bcc` (array, optional)
- `threadId` (string | null, optional): Conversation id of the scheduled email, as listed in the Scheduled folder.
- `scheduled` (boolean, optional): True when the email was scheduled for later with sendAt.
- `attachment` (string, optional): The filename the first attachment was sent under, when one was attached.
- `attachments` (array, optional): Every attachment's filename, in order, as Gmail showed it before sending.
- `scheduledFor` (string | null, optional): The send date and time as Gmail displays it on the Scheduled list, in the account's language.
- `foundInScheduled` (boolean, optional): Whether the email was found on the Scheduled list after scheduling.

## FAQ

### What does "Send Gmail email" do?

Send an email from the signed-in Gmail account, with a plain-text body and up to 10 file attachments in the same email (attachment, attachment2 ... attachment10; name them with attachmentNames). Returns every attachment's name as Gmail showed it before sending. Always starts a new conversation. To answer inside an existing thread, use mail.google.com/reply_to_email.

### How do I automatically send Gmail email on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/send_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/send_email

### Is there a mail.google.com API to send Gmail email?

You do not need one. "Send Gmail email" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: to, subject. Optional: cc, bcc, body, sendAt, account, attachment, attachment2, attachment3, attachment4, attachment5, attachment6, attachment7, attachment8, attachment9, attachment10, attachmentName, attachmentNames, confirmSharingWarning.

### What does it return?

It returns cc, to, bcc, sent, subject, threadId, scheduled, attachment, attachments, scheduledFor, foundInScheduled.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/send_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/send_email

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/send_email
