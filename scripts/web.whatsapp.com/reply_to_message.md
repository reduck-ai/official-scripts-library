# Reply to a WhatsApp message

Automatically reply to a WhatsApp message on web.whatsapp.com. Reply to one WhatsApp message with text, quoting it, given the message's id from get_conversation or get_inbox. The chat is found from the message id. Returns the reply's own id, which delete_message takes, with the time and the delivery status. The run succeeds only when WhatsApp's server has acknowledged the reply and it quotes that message. A message deleted for everyone cannot be replied to. Confirm the text with the user before sending. If WhatsApp Web is open in another tab of the same browser, the run stops and asks to close that tab.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/reply_to_message`
- Updated: 2026-10-22 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/reply_to_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/reply_to_message
```

## Input

- `text` (string, required): The reply text.
- `messageId` (string, required): The message to reply to, as get_conversation or get_inbox returns it in `id`.

## Output

- `id` (string, required): The reply's own message id, usable by delete_message and the other message scripts.
- `sent` (boolean, required): True once WhatsApp's server acknowledged the reply.
- `chatId` (string, required)
- `repliedTo` (string, required): The id of the message quoted.
- `at` (string | null, optional): When it was sent, ISO datetime.
- `text` (string, optional)
- `status` (any, optional): Delivery status when the run ended.

## FAQ

### What does "Reply to a WhatsApp message" do?

Reply to one WhatsApp message with text, quoting it, given the message's id from get_conversation or get_inbox. The chat is found from the message id. Returns the reply's own id, which delete_message takes, with the time and the delivery status. The run succeeds only when WhatsApp's server has acknowledged the reply and it quotes that message. A message deleted for everyone cannot be replied to. Confirm the text with the user before sending. If WhatsApp Web is open in another tab of the same browser, the run stops and asks to close that tab.

### How do I automatically reply to a WhatsApp message on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/reply_to_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/reply_to_message

### Is there a web.whatsapp.com API to reply to a WhatsApp message?

You do not need one. "Reply to a WhatsApp message" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: messageId, text.

### What does it return?

It returns at, id, sent, text, chatId, status, repliedTo.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/reply_to_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/reply_to_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/reply_to_message
