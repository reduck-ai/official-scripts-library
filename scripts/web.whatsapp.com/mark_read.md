# WhatsApp — Mark chat read/unread

Automatically mark chat read/unread on web.whatsapp.com. Mark a chat (by exact name) as read or unread. Safe to repeat: if the chat is already in the desired state, it returns success.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/mark_read`
- Updated: 2026-08-26 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/mark_read`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/mark_read
```

## Input

- `name` (string, required): Exact chat name (from get_inbox).
- `read` (boolean, optional): true = mark as read, false = mark as unread.

## Output

- `name` (string, required)
- `read` (boolean, required)
- `alreadyInState` (boolean, optional): True when the chat was already read/unread as requested and nothing was clicked.

## FAQ

### What does "WhatsApp — Mark chat read/unread" do?

Mark a chat (by exact name) as read or unread. Safe to repeat: if the chat is already in the desired state, it returns success.

### How do I automatically mark chat read/unread on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/mark_read, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/mark_read

### Is there a web.whatsapp.com API to mark chat read/unread?

You do not need one. "WhatsApp — Mark chat read/unread" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name. Optional: read.

### What does it return?

It returns name, read, alreadyInState.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/mark_read, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/mark_read

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/mark_read
