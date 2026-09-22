# WhatsApp — Mute chat

Automatically mute chat on web.whatsapp.com. Mute or unmute notifications for a WhatsApp chat, found by its exact name. When muting, choose how long: 8 hours, 1 week, or always. A chat that is already in the state you asked for is left untouched and reported as a success.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/mute_chat`
- Updated: 2026-08-10 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/mute_chat`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/mute_chat
```

## Input

- `name` (string, required): Exact chat name (from get_inbox).
- `mute` (boolean, optional): true = mute, false = unmute.
- `duration` (string, optional): Mute duration (only used when mute=true).

## Output

- `name` (string, required)
- `muted` (boolean, required)

## FAQ

### What does "WhatsApp — Mute chat" do?

Mute or unmute notifications for a WhatsApp chat, found by its exact name. When muting, choose how long: 8 hours, 1 week, or always. A chat that is already in the state you asked for is left untouched and reported as a success.

### How do I automatically mute chat on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/mute_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/mute_chat

### Is there a web.whatsapp.com API to mute chat?

You do not need one. "WhatsApp — Mute chat" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name. Optional: mute, duration.

### What does it return?

It returns name, muted.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/mute_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/mute_chat

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/mute_chat
