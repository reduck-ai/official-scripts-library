# Send WhatsApp message or attachment

Automatically send WhatsApp message or attachment on web.whatsapp.com. Send a WhatsApp message to a chat, given by its `chatId` from get_inbox, or to a phone number in international format that has no chat yet. The message is a text, an image, a video or a document with an optional caption, or a saved contact's card. Returns the new message's id, which delete_message and react_to_message take, with the time, the delivery status and the account that sent it. The run succeeds only when WhatsApp's server has acknowledged the message, and fails if WhatsApp marks it as failed. With dry_run, the chat is opened and the message prepared, and nothing is sent. Confirm the recipient with the user before sending. If WhatsApp Web is open in another tab of the same browser, the run stops and asks to close that tab.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/send_message`
- Updated: 2026-10-13 (v18)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/send_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/send_message
```

## Input

- `kind` (string, required): What to send: a text, an attached file of that kind, or a saved contact's card.
- `text` (string, optional): The message text, for kind text.
- `phone` (string, optional): Recipient phone in international format, for a number with no chat yet, e.g. "+33 6 12 34 56 78" or "0033612345678". Confirm the number with the user before sending. Give this or `chatId`.
- `chatId` (string, optional): The chat to send to, as get_inbox returns it in `chatId`. Give this or `phone`.
- `caption` (string, optional): Optional caption for an image, video or document.
- `dry_run` (boolean, optional): When true, everything runs up to the send and stops: the chat is opened and checked, the text typed or the file accepted by WhatsApp's editor, the contact found. Nothing is sent.
- `filename` (string, optional): Name the file is sent under, e.g. report.pdf. WhatsApp shows it on documents.
- `attachment` (string, optional): The file to send, for kind image, video or document.
- `contactName` (string, optional): Saved name of the contact whose card to send, exactly as the address book shows it, for kind contact.

## Output

- `kind` (string, required)
- `sent` (boolean, required): True once WhatsApp's server acknowledged the message. False on a dry run.
- `chatId` (string, required): The chat the message went to.
- `at` (string | null, optional): When it was sent, ISO datetime.
- `id` (string | null, optional): The new message's id, usable by delete_message, react_to_message and the other message scripts. Null on a dry run.
- `status` (any, optional): Delivery status when the run ended.
- `dry_run` (boolean, optional)
- `recipient` (string, optional): Chat title, as the chat list shows it.
- `account_used` (string | null, optional): Phone number of the WhatsApp account that sent it, read from the live session.

## FAQ

### What does "Send WhatsApp message or attachment" do?

Send a WhatsApp message to a chat, given by its `chatId` from get_inbox, or to a phone number in international format that has no chat yet. The message is a text, an image, a video or a document with an optional caption, or a saved contact's card. Returns the new message's id, which delete_message and react_to_message take, with the time, the delivery status and the account that sent it. The run succeeds only when WhatsApp's server has acknowledged the message, and fails if WhatsApp marks it as failed. With dry_run, the chat is opened and the message prepared, and nothing is sent. Confirm the recipient with the user before sending. If WhatsApp Web is open in another tab of the same browser, the run stops and asks to close that tab.

### How do I automatically send WhatsApp message or attachment on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/send_message

### Is there a web.whatsapp.com API to send WhatsApp message or attachment?

You do not need one. "Send WhatsApp message or attachment" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: kind. Optional: text, phone, chatId, caption, dry_run, filename, attachment, contactName.

### What does it return?

It returns at, id, kind, sent, chatId, status, dry_run, recipient, account_used.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/send_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/send_message
