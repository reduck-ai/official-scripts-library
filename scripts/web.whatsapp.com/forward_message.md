# Forward a WhatsApp message

Automatically forward a WhatsApp message on web.whatsapp.com. Forward a specific message (by messageId) from one chat to one or more other chats (by exact name). Opens the source chat, forwards via the recipient picker, and confirms completion.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/forward_message`
- Updated: 2026-09-16 (v24)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/forward_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/forward_message
```

## Input

- `name` (string, required): Exact source chat name to open (from get_inbox).
- `toChats` (array, required): Exact names of the destination chats to forward to.
- `messageId` (string, required): Message id to forward (from get_conversation or search_messages). Note: if this message was sent immediately after another message from the same sender with no time gap, WhatsApp may have grouped them into a single row that only exposes the newest message's id — forwarding an earlier, swallowed message in such a group will fail with a clear error. Very old messages in long conversations may also be unreachable.

## Output

- `toChats` (array, required)
- `forwarded` (boolean, required)
- `messageId` (string, required)

## FAQ

### What does "Forward a WhatsApp message" do?

Forward a specific message (by messageId) from one chat to one or more other chats (by exact name). Opens the source chat, forwards via the recipient picker, and confirms completion.

### How do I automatically forward a WhatsApp message on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/forward_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/forward_message

### Is there a web.whatsapp.com API to forward a WhatsApp message?

You do not need one. "Forward a WhatsApp message" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name, messageId, toChats.

### What does it return?

It returns toChats, forwarded, messageId.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/forward_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/forward_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/forward_message
