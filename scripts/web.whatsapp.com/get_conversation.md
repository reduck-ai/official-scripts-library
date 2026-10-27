# Get WhatsApp conversation

Automatically get WhatsApp conversation on web.whatsapp.com. Read the most recent messages of one WhatsApp chat, oldest first. Give the chat by its `chatId` from get_inbox. Each message gives its id, type, sender (in groups), time, text or caption, whether it was deleted for everyone, the delivery status of your own messages, file details for media, and its reactions with counts. `complete` is true when the start of the chat's history was reached. Reading does not open the chat, so nothing is marked as read and the other person gets no read receipt. If WhatsApp Web is open in another tab of the same browser, the run stops and asks to close that tab. If the browser is not linked to WhatsApp, the run stops and says so. An unknown chatId stops the run with an error.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/get_conversation`
- Updated: 2026-10-22 (v26)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/get_conversation`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_conversation
```

## Input

- `chatId` (string, required): The chat's id, as get_inbox returns it in `chatId`.
- `count` (integer, optional): How many of the most recent messages to return.

## Output

- `name` (string, required): Chat title, as the chat list shows it.
- `chatId` (string, required)
- `complete` (boolean, required): True when the start of the chat's history was reached, so no earlier message exists on this device.
- `messages` (array, required): Messages oldest first, ending with the newest one.

## FAQ

### What does "Get WhatsApp conversation" do?

Read the most recent messages of one WhatsApp chat, oldest first. Give the chat by its `chatId` from get_inbox. Each message gives its id, type, sender (in groups), time, text or caption, whether it was deleted for everyone, the delivery status of your own messages, file details for media, and its reactions with counts. `complete` is true when the start of the chat's history was reached. Reading does not open the chat, so nothing is marked as read and the other person gets no read receipt. If WhatsApp Web is open in another tab of the same browser, the run stops and asks to close that tab. If the browser is not linked to WhatsApp, the run stops and says so. An unknown chatId stops the run with an error.

### How do I automatically get WhatsApp conversation on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_conversation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_conversation

### Is there a web.whatsapp.com API to get WhatsApp conversation?

You do not need one. "Get WhatsApp conversation" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: chatId. Optional: count.

### What does it return?

It returns name, chatId, complete, messages.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_conversation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_conversation

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/get_conversation
