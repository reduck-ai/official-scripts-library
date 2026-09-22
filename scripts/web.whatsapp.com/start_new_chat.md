# WhatsApp — Start new chat

Automatically start new chat on web.whatsapp.com. Open a chat with a contact by name, even if you have no existing conversation with them. Returns the opened chat's header name. Throws if the contact isn't found.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/start_new_chat`
- Updated: 2026-09-16 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/start_new_chat`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/start_new_chat
```

## Input

- `contact` (string, required): Contact name (as saved in your contacts) to open a chat with, even with no prior conversation.

## Output

- `opened` (boolean, required)
- `contact` (string, required)
- `chatName` (string | null, required)

## FAQ

### What does "WhatsApp — Start new chat" do?

Open a chat with a contact by name, even if you have no existing conversation with them. Returns the opened chat's header name. Throws if the contact isn't found.

### How do I automatically start new chat on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/start_new_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/start_new_chat

### Is there a web.whatsapp.com API to start new chat?

You do not need one. "WhatsApp — Start new chat" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: contact.

### What does it return?

It returns opened, contact, chatName.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/start_new_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/start_new_chat

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/start_new_chat
