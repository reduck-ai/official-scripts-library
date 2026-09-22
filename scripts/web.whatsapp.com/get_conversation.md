# Get WhatsApp conversation

Automatically get WhatsApp conversation on web.whatsapp.com. Open a WhatsApp chat by its exact name (as returned by get_inbox) and return its messages in chronological order: sender, direction (sent/received), time, date, text and media type. `count` = how many recent messages to load (scrolls up for older). A message that was deleted for everyone is still returned, flagged with `deleted: true` and carrying no text, so it is never mistaken for a message that could not be read.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/get_conversation`
- Updated: 2026-09-16 (v21)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/get_conversation`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_conversation
```

## Input

- `name` (string, required): Exact chat/contact/group name to open (the `name` field from get_inbox).
- `count` (integer, optional): How many most-recent messages to return (scrolls up to load older).

## FAQ

### What does "Get WhatsApp conversation" do?

Open a WhatsApp chat by its exact name (as returned by get_inbox) and return its messages in chronological order: sender, direction (sent/received), time, date, text and media type. `count` = how many recent messages to load (scrolls up for older). A message that was deleted for everyone is still returned, flagged with `deleted: true` and carrying no text, so it is never mistaken for a message that could not be read.

### How do I automatically get WhatsApp conversation on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_conversation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_conversation

### Is there a web.whatsapp.com API to get WhatsApp conversation?

You do not need one. "Get WhatsApp conversation" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name. Optional: count.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_conversation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_conversation

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/get_conversation
