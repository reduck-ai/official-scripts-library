# Send Telegram message or document

Automatically send Telegram message or document on web.telegram.org. Send a text message, a document, or a document with a caption to a Telegram conversation identified by its peer id (the id get_inbox returns), optionally as a reply. Confirms the send by finding the outgoing bubble in the conversation afterwards rather than trusting the click, reading back the document's filename and size and requiring the quoted-message embed when a reply was asked for, and reports whether the same message or file was already there plus which account sent it. Refuses conversations with no composer, such as broadcast channels you do not administer.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/send_message`
- Updated: 2026-09-22 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/send_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/send_message
```

## Input

- `peerId` (string, required): The conversation's peer id, as returned by get_inbox (e.g. "8591421602" for Saved Messages; negative ids are channels and groups). Confirm the target with the user before sending — a peer id is not human-readable, so echo back the chatTitle this returns.
- `text` (string, optional): The message text. Required on its own for a text message; sent as the document's caption when a file is also given. Omit for a document with no caption.
- `filename` (string, optional): Required with fileBase64: the name Telegram gives the document, including its extension (e.g. "report.pdf"). Also what the script verifies the sent bubble against. Not used with the `attachment` input, which is sent under its own name.
- `attachment` (string, optional): A file to send as a document, bound through the platform's own file channel. Preferred over fileBase64: it carries the bytes outside the argument payload, so it is not limited by the request size. Telegram has no file input of its own, so the file is landed on a throwaway input the script creates and then handed to Telegram's paste handler — which means it is sent under the name 'attachment'. Use fileBase64 when the stored filename matters.
- `fileBase64` (string, optional): Optional: base64 of a file's bytes, to send it as a document. Requires filename. Prefer the `attachment` input, which has no payload ceiling. Keep this modest (a few MB); the base64 travels inside the request.
- `replyToMessageId` (string, optional): Optional: send this as a reply to an existing message, given its id from get_conversation. Works for both a text message and a document. This is why there is no separate reply script — on Telegram a reply is an ordinary message carrying a reply-to reference.

## Output

- `kind` (string, required): Which of the two sends ran: "document" when fileBase64 was supplied, otherwise "text".
- `sent` (boolean, required): True once an outgoing bubble matching what was sent, and carrying a server-assigned id, was found in the conversation.
- `peerId` (string, required): The peer id that was actually opened, read back from the address bar.
- `account_used` (string | null, required): The account that actually sent it, read from the app's own account menu rather than assumed from the request. Null if the menu did not expose a name.
- `verified_on_page` (boolean, required): True when the send was confirmed by finding the bubble in the conversation afterwards, rather than assumed from the keypress or the button click.
- `id` (string | null, optional): Telegram's server-assigned message id. The script waits for the real integer id rather than the optimistic local one Telegram renders while the send is pending, so this is always usable by delete/react/reply. For a document it also means the upload finished.
- `text` (string | null, optional): The text that was sent, or the caption for a document. Null for a document sent without a caption.
- `fileSize` (string | null, optional): The size Telegram renders on the sent document bubble, read back from the page ("19.0B", "1.2 KB"). Compare it against the bytes you sent to confirm the whole file landed. Null for a text message.
- `filename` (string | null, optional): The document's filename, or null for a text message.
- `chatTitle` (string | null, optional): The conversation title from the header — echo this to a human, since a peer id is not recognisable.
- `repliedTo` (string | null, optional): The message id this was sent as a reply to, or null for a normal message. Evidence-backed rather than echoed: when a reply was requested the script only accepts a sent bubble that actually carries the quoted-message embed, so a reply reference dropped by the attachment dialog fails loudly instead of being reported as done.
- `already_present` (boolean, optional): Whether an outgoing message with exactly this text (or a document with this filename) was already in the conversation beforehand. Reported, not enforced — resending is legitimate — so the caller decides what to do about a duplicate.

## FAQ

### What does "Send Telegram message or document" do?

Send a text message, a document, or a document with a caption to a Telegram conversation identified by its peer id (the id get_inbox returns), optionally as a reply. Confirms the send by finding the outgoing bubble in the conversation afterwards rather than trusting the click, reading back the document's filename and size and requiring the quoted-message embed when a reply was asked for, and reports whether the same message or file was already there plus which account sent it. Refuses conversations with no composer, such as broadcast channels you do not administer.

### How do I automatically send Telegram message or document on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/send_message

### Is there a web.telegram.org API to send Telegram message or document?

You do not need one. "Send Telegram message or document" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Required: peerId. Optional: text, filename, attachment, fileBase64, replyToMessageId.

### What does it return?

It returns id, kind, sent, text, peerId, fileSize, filename, chatTitle, repliedTo, account_used, already_present, verified_on_page.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It makes changes on web.telegram.org, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/send_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/send_message
