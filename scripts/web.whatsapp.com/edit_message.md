# Edit a WhatsApp message

Automatically edit a WhatsApp message on web.whatsapp.com. Edit one of your own recently-sent messages (by messageId) with new text. Edit is only allowed within ~15 min of sending; the script fails loudly if the Edit option isn't available. Verifies the new text is shown.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/edit_message`
- Updated: 2026-09-16 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/edit_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/edit_message
```

## Input

- `name` (string, required): Exact chat name to open (from get_inbox).
- `text` (string, required): New text to replace the message with.
- `messageId` (string, required): Message id (data-id) of your message to edit.

## Output

- `text` (string, required)
- `edited` (boolean, required)
- `messageId` (string, required)

## FAQ

### What does "Edit a WhatsApp message" do?

Edit one of your own recently-sent messages (by messageId) with new text. Edit is only allowed within ~15 min of sending; the script fails loudly if the Edit option isn't available. Verifies the new text is shown.

### How do I automatically edit a WhatsApp message on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/edit_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/edit_message

### Is there a web.whatsapp.com API to edit a WhatsApp message?

You do not need one. "Edit a WhatsApp message" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name, messageId, text.

### What does it return?

It returns text, edited, messageId.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/edit_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/edit_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/edit_message
