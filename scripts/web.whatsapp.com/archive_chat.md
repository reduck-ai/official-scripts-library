# WhatsApp — Archive chat

Automatically archive chat on web.whatsapp.com. Archive or unarchive a chat by exact name. Archived chats still appear in search. Safe to repeat: returns success if the chat is already in the desired state.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/archive_chat`
- Updated: 2026-08-27 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/archive_chat`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/archive_chat
```

## Input

- `name` (string, required): Exact chat name (from get_inbox).
- `archive` (boolean, optional): true = archive, false = unarchive.

## Output

- `name` (string, required)
- `archived` (boolean, required)
- `alreadyInState` (boolean, optional): True when the chat was already archived/unarchived as requested and nothing was clicked.

## FAQ

### What does "WhatsApp — Archive chat" do?

Archive or unarchive a chat by exact name. Archived chats still appear in search. Safe to repeat: returns success if the chat is already in the desired state.

### How do I automatically archive chat on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/archive_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/archive_chat

### Is there a web.whatsapp.com API to archive chat?

You do not need one. "WhatsApp — Archive chat" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name. Optional: archive.

### What does it return?

It returns name, archived, alreadyInState.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/archive_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/archive_chat

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/archive_chat
