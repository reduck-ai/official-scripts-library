# Get WhatsApp message reactions

Automatically get WhatsApp message reactions on web.whatsapp.com. Get the emoji reactions on a specific WhatsApp message (by messageId, from get_conversation/search_messages), including who reacted with each emoji. Opens the reaction badge's "View reactions" popup, reads each distinct emoji's tab (emoji + count) and, per tab, the reactor names. Returns { messageId, reactions: [] } if the message has no reactions.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/get_message_reactions`
- Updated: 2026-09-16 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/get_message_reactions`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_message_reactions
```

## Input

- `name` (string, required): Exact chat name to open (as returned by get_inbox).
- `messageId` (string, required): Message id (data-id) to read reactions from, from get_conversation/search_messages.

## Output

- `messageId` (string, required)
- `reactions` (array, required)

## FAQ

### What does "Get WhatsApp message reactions" do?

Get the emoji reactions on a specific WhatsApp message (by messageId, from get_conversation/search_messages), including who reacted with each emoji. Opens the reaction badge's "View reactions" popup, reads each distinct emoji's tab (emoji + count) and, per tab, the reactor names. Returns { messageId, reactions: [] } if the message has no reactions.

### How do I automatically get WhatsApp message reactions on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_message_reactions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_message_reactions

### Is there a web.whatsapp.com API to get WhatsApp message reactions?

You do not need one. "Get WhatsApp message reactions" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name, messageId.

### What does it return?

It returns messageId, reactions.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

Unknown: its author has not declared whether it changes anything on web.whatsapp.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_message_reactions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_message_reactions

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/get_message_reactions
