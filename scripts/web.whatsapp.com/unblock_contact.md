# WhatsApp — Unblock contact

Automatically unblock contact on web.whatsapp.com. Unblock a previously-blocked WhatsApp contact by exact chat name. Safe to repeat: does nothing if the contact isn't blocked.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/unblock_contact`
- Updated: 2026-08-27 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/unblock_contact`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/unblock_contact
```

## Input

- `name` (string, required): Exact contact/chat name to unblock (from get_inbox).

## Output

- `recipient` (string, required)
- `unblocked` (boolean, required)
- `alreadyUnblocked` (boolean, required): True when the contact was not blocked and nothing was clicked.

## FAQ

### What does "WhatsApp — Unblock contact" do?

Unblock a previously-blocked WhatsApp contact by exact chat name. Safe to repeat: does nothing if the contact isn't blocked.

### How do I automatically unblock contact on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/unblock_contact, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/unblock_contact

### Is there a web.whatsapp.com API to unblock contact?

You do not need one. "WhatsApp — Unblock contact" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name.

### What does it return?

It returns recipient, unblocked, alreadyUnblocked.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/unblock_contact, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/unblock_contact

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/unblock_contact
