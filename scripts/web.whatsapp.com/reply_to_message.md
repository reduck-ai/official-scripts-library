# Reply to a WhatsApp message

Automatically reply to a WhatsApp message on web.whatsapp.com. Reply (quote) to a specific message by messageId in a chat, then send text. Confirms the quote context attached before sending, and confirms delivery via WhatsApp's own status indicator — not just the outgoing bubble appearing — throwing if WhatsApp reports the send failed.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/reply_to_message`
- Updated: 2026-09-16 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/reply_to_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/reply_to_message
```

## Input

- `name` (string, required): Exact chat name to open (from get_inbox).
- `text` (string, required): The reply text to send.
- `messageId` (string, required): Message id to reply to (from get_conversation or search_messages). Note: if this message was sent immediately after another message from the same sender with no time gap, WhatsApp may have grouped them into a single row that only exposes the newest message's id — replying to an earlier, swallowed message in such a group will fail with a clear error. Very old messages in long conversations may also be unreachable.

## Output

- `sent` (boolean, required): True once the reply is confirmed sent: the outgoing bubble appeared and WhatsApp itself did not flag it as failed to send.
- `text` (string, required)
- `repliedTo` (string, required)

## FAQ

### What does "Reply to a WhatsApp message" do?

Reply (quote) to a specific message by messageId in a chat, then send text. Confirms the quote context attached before sending, and confirms delivery via WhatsApp's own status indicator — not just the outgoing bubble appearing — throwing if WhatsApp reports the send failed.

### How do I automatically reply to a WhatsApp message on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/reply_to_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/reply_to_message

### Is there a web.whatsapp.com API to reply to a WhatsApp message?

You do not need one. "Reply to a WhatsApp message" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name, messageId, text.

### What does it return?

It returns sent, text, repliedTo.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/reply_to_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/reply_to_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/reply_to_message
