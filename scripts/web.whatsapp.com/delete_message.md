# WhatsApp API: delete a message

Automatically delete a message on web.whatsapp.com. Delete one WhatsApp message by id, for yourself or for everyone, and confirm it is gone.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/delete_message`
- Updated: 2026-10-05 (v23)
- Author: Reduck AI (reduck)

## About

Most people want this a minute after sending something to the wrong chat. Say you sent a client the wrong invoice PDF an hour ago. Your agent pulls the last 20 messages, finds that bubble and deletes it for everyone, so the client sees a deleted-message placeholder instead of the file. In a group where you are an admin, the same call removes a member's spam link. Everyone is only offered for about two days after sending, and an admin deleting someone else's message gets an extra warning that the author will see who did it. After the click, the run checks that the message no longer appears in the chat. For scope me it also waits 12 seconds and reloads, because a local delete can come back if it has not been saved yet. Deleting is permanent, so confirm with the user before using everyone.

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

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "scope": "…",
  "deleted": true,
  "messageId": "abc123",
  "recipient": "…"
}
```

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

It makes changes on web.whatsapp.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/delete_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/delete_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can I delete WhatsApp messages older than two days?

Only for yourself. Past the roughly two-day window the dialog offers Delete for me alone, so use scope me. A call with scope everyone throws and deletes nothing. The run also has to find the message first, scrolling the chat back up to 40 times and stopping sooner if no older messages load. A message further back than that is reported as not found, and WhatsApp Web only holds part of your history anyway.

### Can I delete a message someone else sent me?

From your own view only, with scope me. Removing another person's message for everyone works only in a group where you are an admin, within about two days of it being posted. Otherwise the call stops with an error and nothing is deleted.

### What happens when an admin deletes a member's message?

WhatsApp shows the admin a second confirmation first, warning that the author will see the message was deleted by them. The run clicks through that dialog only when the scope is everyone.

### Can it clear a whole conversation?

No, it deletes one message per call. To empty a chat use clear_chat, and to remove the conversation use delete_chat.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/delete_message
