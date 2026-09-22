# Star a WhatsApp message

Automatically star a WhatsApp message on web.whatsapp.com. Star or unstar a specific message (by messageId) in a chat. Safe to repeat: it returns success if the message is already in the desired state. Starred messages are readable via get_starred_messages.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/star_message`
- Updated: 2026-09-16 (v12)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/star_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/star_message
```

## Input

- `name` (string, required): Exact chat name (from get_inbox).
- `messageId` (string, required): Message id (data-id) to star/unstar.
- `star` (boolean, optional): true = star, false = unstar.

## Output

- `starred` (boolean, required)
- `messageId` (string, required)

## FAQ

### What does "Star a WhatsApp message" do?

Star or unstar a specific message (by messageId) in a chat. Safe to repeat: it returns success if the message is already in the desired state. Starred messages are readable via get_starred_messages.

### How do I automatically star a WhatsApp message on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/star_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/star_message

### Is there a web.whatsapp.com API to star a WhatsApp message?

You do not need one. "Star a WhatsApp message" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name, messageId. Optional: star.

### What does it return?

It returns starred, messageId.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/star_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/star_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/star_message
