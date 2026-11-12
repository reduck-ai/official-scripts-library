# Send Telegram message or document

Automatically send Telegram message or document on web.telegram.org. Send a text message, a document, or a document with a caption to a Telegram conversation, by its peer id from get_inbox, optionally as a reply. Returns the id Telegram's server gave the message, the text or file name and size Telegram holds, the account that sent it, and whether the same message or file was already among the recent ones. Refuses a conversation this account cannot post in, such as a channel it does not administer. Confirm the conversation with the user before sending.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/send_message`
- Updated: 2026-11-11 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/send_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/send_message
```

## Input

- `peerId` (string, required): The conversation, as web.telegram.org/get_inbox returns it (your own account id is Saved Messages). Confirm the target with the user before sending, and show them the chatTitle this returns.
- `text` (string, optional): The message text. With a file, it is sent as the file's caption.
- `filename` (string, optional): Required with fileBase64: the document's name, with its extension.
- `attachment` (string, optional): A file to send as a document. Preferred over fileBase64. It is sent under the name 'attachment'; use fileBase64 with filename when the name matters.
- `fileBase64` (string, optional): A file's bytes as base64, sent as a document. Requires filename. Keep it to a few MB.
- `replyToMessageId` (string, optional): Send as a reply to this message, by the id get_conversation returns. The message must be among the most recent ones of the conversation.

## Output

- `id` (string, required): The message id Telegram's server assigned, which delete_message and replyToMessageId take.
- `kind` (string, required)
- `sent` (boolean, required): True once Telegram's server holds the message.
- `peerId` (string, required)
- `account_used` (string | null, required): The name of the account that sent it.
- `text` (string | null, optional): The text or caption Telegram holds for the message.
- `fileSize` (integer | null, optional): The size in bytes Telegram holds for the document.
- `filename` (string | null, optional)
- `accountId` (string, optional)
- `chatTitle` (string | null, optional): The conversation's name: show it to the user, since a peer id is not readable.
- `repliedTo` (string | null, optional): The id of the message this one replies to, as Telegram holds it.
- `already_present` (boolean, optional): Whether a message of this account with the same text (or a document with the same name) was already among the most recent ones before this send. Reported, not enforced.

## FAQ

### What does "Send Telegram message or document" do?

Send a text message, a document, or a document with a caption to a Telegram conversation, by its peer id from get_inbox, optionally as a reply. Returns the id Telegram's server gave the message, the text or file name and size Telegram holds, the account that sent it, and whether the same message or file was already among the recent ones. Refuses a conversation this account cannot post in, such as a channel it does not administer. Confirm the conversation with the user before sending.

### How do I automatically send Telegram message or document on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/send_message

### Is there a web.telegram.org API to send Telegram message or document?

You do not need one. "Send Telegram message or document" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Required: peerId. Optional: text, filename, attachment, fileBase64, replyToMessageId.

### What does it return?

It returns id, kind, sent, text, peerId, fileSize, filename, accountId, chatTitle, repliedTo, account_used, already_present.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It makes changes on web.telegram.org, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/send_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/send_message
