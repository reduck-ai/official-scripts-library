# React to a WhatsApp message

Automatically react to a WhatsApp message on web.whatsapp.com. React to a specific message (by messageId, from get_conversation/search_messages) in a chat with an emoji. Uses the quick-reaction bar; falls back to the full picker. Verifies the reaction was applied. Re-reacting the same emoji toggles it off.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/react_to_message`
- Updated: 2026-09-16 (v17)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/react_to_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/react_to_message
```

## Input

- `name` (string, required): Exact chat name to open (as returned by get_inbox).
- `emoji` (string, required): Emoji to react with, e.g. 👍 ❤️ 😂 😮 😢 🙏. Quick-bar emojis are most reliable.
- `messageId` (string, required): Message id (data-id) to react to.

## Output

- `emoji` (string, required)
- `reacted` (boolean, required)
- `messageId` (string, required)

## FAQ

### What does "React to a WhatsApp message" do?

React to a specific message (by messageId, from get_conversation/search_messages) in a chat with an emoji. Uses the quick-reaction bar; falls back to the full picker. Verifies the reaction was applied. Re-reacting the same emoji toggles it off.

### How do I automatically react to a WhatsApp message on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/react_to_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/react_to_message

### Is there a web.whatsapp.com API to react to a WhatsApp message?

You do not need one. "React to a WhatsApp message" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name, messageId, emoji.

### What does it return?

It returns emoji, reacted, messageId.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/react_to_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/react_to_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/react_to_message
