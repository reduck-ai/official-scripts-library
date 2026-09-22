# WhatsApp — Clear chat

Automatically clear chat on web.whatsapp.com. Clear all messages from a WhatsApp chat by exact name (the chat stays in your list, just emptied). Optional keepStarred to preserve starred messages. This permanently empties the chat and is only briefly undoable via WhatsApp's own toast.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/clear_chat`
- Updated: 2026-08-26 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/clear_chat`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/clear_chat
```

## Input

- `name` (string, required): Exact chat/contact/group name to clear (from get_inbox).
- `keepStarred` (boolean, optional): Keep starred messages instead of clearing them too. With this set the chat does not end up empty, so the emptiness verification is skipped for that branch.

## Output

- `cleared` (boolean, required)
- `recipient` (string, required)
- `verified_empty` (boolean | null, optional): True when the chat was re-read after clearing and held no message rows. Null when keepStarred was set, since the chat legitimately keeps its starred messages.
- `messages_before` (integer | null, optional): Message rows present before clearing, as evidence the chat was non-empty and the clear actually did something.

## FAQ

### What does "WhatsApp — Clear chat" do?

Clear all messages from a WhatsApp chat by exact name (the chat stays in your list, just emptied). Optional keepStarred to preserve starred messages. This permanently empties the chat and is only briefly undoable via WhatsApp's own toast.

### How do I automatically clear chat on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/clear_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/clear_chat

### Is there a web.whatsapp.com API to clear chat?

You do not need one. "WhatsApp — Clear chat" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name. Optional: keepStarred.

### What does it return?

It returns cleared, recipient, verified_empty, messages_before.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/clear_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/clear_chat

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/clear_chat
