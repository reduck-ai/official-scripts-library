# Get WhatsApp inbox

Automatically get WhatsApp inbox on web.whatsapp.com. List the WhatsApp chat list (inbox): for each chat its name, date/time label, read/unread status, unread message count and last-message snippet. Ordered top→down (most recent first). `count` caps how many chats to return.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/get_inbox`
- Updated: 2026-09-17 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/get_inbox`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_inbox
```

## Input

- `count` (integer, optional): Max number of chats to return, from the top of the list.
- `since` (string, optional): Optional ISO datetime. Return only chats whose last activity is at or after this instant, which is how a caller polls for new messages. Chats whose timestamp could not be resolved are always returned, never silently dropped.

## FAQ

### What does "Get WhatsApp inbox" do?

List the WhatsApp chat list (inbox): for each chat its name, date/time label, read/unread status, unread message count and last-message snippet. Ordered top→down (most recent first). `count` caps how many chats to return.

### How do I automatically get WhatsApp inbox on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_inbox

### Is there a web.whatsapp.com API to get WhatsApp inbox?

You do not need one. "Get WhatsApp inbox" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Optional: count, since.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_inbox

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/get_inbox
