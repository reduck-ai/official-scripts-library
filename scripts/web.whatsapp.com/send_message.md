# Send WhatsApp message or attachment

Automatically send WhatsApp message or attachment on web.whatsapp.com. Send a WhatsApp message to a chat picked either by its exact name (as returned by get_inbox) or by phone number in international format, which needs no saved contact. The message is either text, an attached image, video or document with an optional caption, or a saved contact's card. Confirms the send by inspecting the conversation afterwards — a delivery tick for text, a cleared upload for an attachment, the contact's own bubble for a card — and throws if WhatsApp flagged it as failed or left it stuck, rather than trusting the bubble appearing. Returns the message id, the account that sent it, and whether identical text was already in the conversation beforehand. Attachment bytes must be supplied inline, since they cannot be fetched from a URL at run time.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/send_message`
- Updated: 2026-09-22 (v15)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/send_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/send_message
```

## Input

- `kind` (string, required): What to send: a plain text message, an attached file of the given kind, or a saved contact's card.
- `name` (string, optional): Exact chat/contact/group name to send to (the `name` field from get_inbox). Provide this OR `phone`, not both.
- `text` (string, optional): Message text. Required when kind is "text".
- `phone` (string, optional): Recipient phone in international format, no saved contact needed. Confirm this number with the user before running; don't guess or reuse a number from context without checking. Non-digits are stripped, a leading "00" international prefix is removed, and a national number (leading trunk 0) is rejected with a clear error. e.g. "+1 555 123 4567", "15551234567" or "0015551234567". Provide this OR `name`, not both.
- `caption` (string, optional): Optional caption for image/video/document.
- `filename` (string, optional): Filename to send it as, e.g. photo.png / clip.mp4 / file.pdf. Required when kind is image/video/document. With the `attachment` file input the bytes are taken from that input, but this name is still what the send is verified against.
- `mimeType` (string, optional): MIME type; inferred from kind + filename extension when omitted.
- `attachment` (string, optional): The file to send, bound through the platform's own file channel and handed to WhatsApp's hidden file input directly. Preferred over fileBase64: it carries the bytes outside the argument payload, so it is not limited by the request size. Use with kind image/video/document; WhatsApp still picks the input by kind, so the kind must match the file.
- `fileBase64` (string, optional): File contents, base64-encoded (no data: prefix), as an alternative to the `attachment` file input. The bytes ride inside the request, so a large file is limited by whatever the caller's own transport allows inline.
- `contactName` (string, optional): The saved name of the contact whose card to send, exactly as WhatsApp's address book shows it. Every phone number saved for that contact is included. Required when kind is "contact".

## Output

- `kind` (string, required): What was sent: "text", "image", "video", "document" or "contact".
- `sent` (boolean, required): True once the send is confirmed: for text, a delivery tick appeared and WhatsApp did not flag a failure; for an attachment, the upload cleared its pending state and stayed unflagged through a settle window; for a contact card, the outgoing bubble naming the contact appeared unflagged.
- `recipient` (string, required): The chat name the message was sent to, read back from the conversation header.
- `account_used` (string | null, required): The phone number of the WhatsApp account that actually sent this, read back from the live session rather than taken from the request.
- `verified_on_page` (boolean, required): True when the send was confirmed by inspecting the conversation afterwards, rather than assumed from the click.
- `id` (string | null, optional): WhatsApp message id of the message that was sent. Populated for every kind.
- `text` (string | null, optional): The text that was sent; null for attachment and contact sends.
- `time` (string | null, optional): Timestamp of the sent message as shown in the bubble (e.g. "3:14 PM"); null for attachment and contact sends.
- `caption` (string | null, optional): The caption sent with the attachment, or null.
- `filename` (string | null, optional): The filename the attachment was sent as, or null for text and contact sends.
- `contactName` (string | null, optional): The saved contact whose card was sent, or null for other kinds.
- `numbersSent` (integer | null, optional): How many of the contact's phone numbers the card carried, counted on WhatsApp's own confirmation screen. Null for other kinds.
- `already_present` (boolean | null, optional): Whether an outgoing message with exactly this text was already in the conversation before this send. Reported, not enforced - re-sending the same text is legitimate. Null for image/video and contact sends, where no comparable content is visible in the bubble.

## FAQ

### What does "Send WhatsApp message or attachment" do?

Send a WhatsApp message to a chat picked either by its exact name (as returned by get_inbox) or by phone number in international format, which needs no saved contact. The message is either text, an attached image, video or document with an optional caption, or a saved contact's card. Confirms the send by inspecting the conversation afterwards — a delivery tick for text, a cleared upload for an attachment, the contact's own bubble for a card — and throws if WhatsApp flagged it as failed or left it stuck, rather than trusting the bubble appearing. Returns the message id, the account that sent it, and whether identical text was already in the conversation beforehand. Attachment bytes must be supplied inline, since they cannot be fetched from a URL at run time.

### How do I automatically send WhatsApp message or attachment on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/send_message

### Is there a web.whatsapp.com API to send WhatsApp message or attachment?

You do not need one. "Send WhatsApp message or attachment" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: kind. Optional: name, text, phone, caption, filename, mimeType, attachment, fileBase64, contactName.

### What does it return?

It returns id, kind, sent, text, time, caption, filename, recipient, contactName, numbersSent, account_used, already_present, verified_on_page.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/send_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/send_message
