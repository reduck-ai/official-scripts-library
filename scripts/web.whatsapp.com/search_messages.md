# Search WhatsApp messages

Automatically search WhatsApp messages on web.whatsapp.com. Global keyword search across all WhatsApp chats. Returns matching messages with the chat name, date label, matched snippet and message id. WhatsApp Web caps how many message hits it surfaces; older ones are only on the phone.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/search_messages`
- Updated: 2026-09-16 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/search_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/search_messages
```

## Input

- `query` (string, required): Keyword(s) to search for across all conversations.
- `count` (integer, optional): Max number of message hits to return.

## FAQ

### What does "Search WhatsApp messages" do?

Global keyword search across all WhatsApp chats. Returns matching messages with the chat name, date label, matched snippet and message id. WhatsApp Web caps how many message hits it surfaces; older ones are only on the phone.

### How do I automatically search WhatsApp messages on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/search_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/search_messages

### Is there a web.whatsapp.com API to search WhatsApp messages?

You do not need one. "Search WhatsApp messages" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: count.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

Unknown: its author has not declared whether it changes anything on web.whatsapp.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/search_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/search_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/search_messages
