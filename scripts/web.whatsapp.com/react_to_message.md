# React to a WhatsApp message

Automatically react to a WhatsApp message on web.whatsapp.com. React to one WhatsApp message with an emoji, given the message's id from get_conversation, get_inbox or send_message. The reaction replaces any reaction you already put on that message. The run succeeds only when WhatsApp records your reaction on the message. The other participants see the reaction. If WhatsApp Web is open in another tab of the same browser, the run stops and asks to close that tab.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/react_to_message`
- Updated: 2026-10-22 (v19)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/react_to_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/react_to_message
```

## Input

- `emoji` (string, required): The emoji to react with, e.g. 👍 ❤️ 😂 😮 😢 🙏. It replaces any reaction you already put on this message.
- `messageId` (string, required): The message's id, as get_conversation or get_inbox returns it.

## Output

- `emoji` (string, required)
- `reacted` (boolean, required): True once the app records your reaction on the message.
- `messageId` (string, required)
- `chatId` (string, optional)

## FAQ

### What does "React to a WhatsApp message" do?

React to one WhatsApp message with an emoji, given the message's id from get_conversation, get_inbox or send_message. The reaction replaces any reaction you already put on that message. The run succeeds only when WhatsApp records your reaction on the message. The other participants see the reaction. If WhatsApp Web is open in another tab of the same browser, the run stops and asks to close that tab.

### How do I automatically react to a WhatsApp message on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/react_to_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/react_to_message

### Is there a web.whatsapp.com API to react to a WhatsApp message?

You do not need one. "React to a WhatsApp message" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: messageId, emoji.

### What does it return?

It returns emoji, chatId, reacted, messageId.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/react_to_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/react_to_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/react_to_message
