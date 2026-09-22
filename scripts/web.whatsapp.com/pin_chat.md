# WhatsApp — Pin chat

Automatically pin chat on web.whatsapp.com. Pin or unpin a chat (by exact name) to/from the top of the chat list. Safe to repeat: if the chat is already in the desired state, it returns success. WhatsApp allows at most 3 pinned chats.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/pin_chat`
- Updated: 2026-08-27 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/pin_chat`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/pin_chat
```

## Input

- `name` (string, required): Exact chat name (from get_inbox).
- `pin` (boolean, optional): true = pin, false = unpin.

## Output

- `name` (string, required)
- `pinned` (boolean, required)

## FAQ

### What does "WhatsApp — Pin chat" do?

Pin or unpin a chat (by exact name) to/from the top of the chat list. Safe to repeat: if the chat is already in the desired state, it returns success. WhatsApp allows at most 3 pinned chats.

### How do I automatically pin chat on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/pin_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/pin_chat

### Is there a web.whatsapp.com API to pin chat?

You do not need one. "WhatsApp — Pin chat" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name. Optional: pin.

### What does it return?

It returns name, pinned.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/pin_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/pin_chat

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/pin_chat
