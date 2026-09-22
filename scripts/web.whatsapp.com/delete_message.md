# WhatsApp API: delete a message

Automatically delete a message on web.whatsapp.com. Delete a specific message (by messageId) in a chat, for yourself or for everyone. "everyone" works on your own recent messages within WhatsApp's ~2-day window, or — if you're a group admin — on any other member's message in that group too; fails loudly if the option isn't offered. Verifies the message was actually removed (not just an optimistic UI change) before returning. Deletion, especially scope:"everyone", is irreversible and visible to other participants (an admin deleting someone else's message even shows them "You deleted this message as admin"). Calling agents should get explicit user confirmation before invoking this with scope:"everyone", and before deleting any message the calling user did not author themselves.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/delete_message`
- Updated: 2026-09-18 (v23)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/delete_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/delete_message
```

## Input

- `name` (string, required): Exact chat/contact/group name containing the message, as WhatsApp lists it in the chat list (an unsaved contact is titled by phone number).
- `scope` (any, required): "everyone" works on your own messages within WhatsApp's ~2-day window, or (if you're a group admin) on any other member's message in that group; throws if not offered. "me" removes it from your view only.
- `messageId` (string, required): Message id (the id/data-id from get_conversation or search_messages; a short-form id without the fromMe_chatId_ prefix is also accepted).

## Output

- `scope` (string, required)
- `deleted` (boolean, required)
- `messageId` (string, required)
- `recipient` (string, required)

## FAQ

### What does "WhatsApp API: delete a message" do?

Delete a specific message (by messageId) in a chat, for yourself or for everyone. "everyone" works on your own recent messages within WhatsApp's ~2-day window, or — if you're a group admin — on any other member's message in that group too; fails loudly if the option isn't offered. Verifies the message was actually removed (not just an optimistic UI change) before returning. Deletion, especially scope:"everyone", is irreversible and visible to other participants (an admin deleting someone else's message even shows them "You deleted this message as admin"). Calling agents should get explicit user confirmation before invoking this with scope:"everyone", and before deleting any message the calling user did not author themselves.

### How do I automatically delete a message on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/delete_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/delete_message

### Is there a web.whatsapp.com API to delete a message?

You do not need one. "WhatsApp API: delete a message" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name, messageId, scope.

### What does it return?

It returns scope, deleted, messageId, recipient.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/delete_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/delete_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/delete_message
