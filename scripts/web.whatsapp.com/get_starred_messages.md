# Get starred WhatsApp messages

Automatically get starred WhatsApp messages on web.whatsapp.com. Open Menu → Starred messages and list all starred messages: the chat they belong to, sender, text, time and date. Returns [] if none are starred.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/get_starred_messages`
- Updated: 2026-09-16 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/get_starred_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_starred_messages
```

## Input

- `count` (integer, optional): Max number of starred messages to return.

## FAQ

### What does "Get starred WhatsApp messages" do?

Open Menu → Starred messages and list all starred messages: the chat they belong to, sender, text, time and date. Returns [] if none are starred.

### How do I automatically get starred WhatsApp messages on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_starred_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_starred_messages

### Is there a web.whatsapp.com API to get starred WhatsApp messages?

You do not need one. "Get starred WhatsApp messages" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Optional: count.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_starred_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_starred_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/get_starred_messages
