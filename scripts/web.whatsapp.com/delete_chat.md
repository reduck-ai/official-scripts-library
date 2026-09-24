# WhatsApp — Delete chat

Automatically delete chat on web.whatsapp.com. Delete a WhatsApp chat by exact name — removes the whole conversation from your chat list and from all your devices, and confirms afterwards that it is really gone. This permanently deletes the conversation and cannot be undone, so the exact chat name should be confirmed with the user before running it rather than inferred or guessed. A group you are still a member of cannot be deleted until you leave it, and that case is reported as a clear error.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/delete_chat`
- Updated: 2026-09-22 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/delete_chat`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/delete_chat
```

## Input

- `name` (string, required): Exact chat/contact/group name to delete (from get_inbox).

## Output

- `deleted` (boolean, required)
- `recipient` (string, required)
- `verified_on_page` (boolean, required): The chat list was re-checked after the deletion and the conversation is no longer present.

## FAQ

### What does "WhatsApp — Delete chat" do?

Delete a WhatsApp chat by exact name — removes the whole conversation from your chat list and from all your devices, and confirms afterwards that it is really gone. This permanently deletes the conversation and cannot be undone, so the exact chat name should be confirmed with the user before running it rather than inferred or guessed. A group you are still a member of cannot be deleted until you leave it, and that case is reported as a clear error.

### How do I automatically delete chat on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/delete_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/delete_chat

### Is there a web.whatsapp.com API to delete chat?

You do not need one. "WhatsApp — Delete chat" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name.

### What does it return?

It returns deleted, recipient, verified_on_page.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/delete_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/delete_chat

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/delete_chat
