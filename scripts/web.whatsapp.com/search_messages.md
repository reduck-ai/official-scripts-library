# Search WhatsApp messages

Automatically search WhatsApp messages on web.whatsapp.com. Search WhatsApp messages by words, in every chat or inside one chat given by its `chatId` from get_inbox. Returns the matching messages, newest first, each with its id, chat, sender (in groups), time and text, so a hit feeds get_conversation and the message scripts. Results come in pages: ask the next page while `complete` is false. A page can hold fewer results than asked. An empty list means nothing matched. Searching opens no chat and marks nothing as read. The search covers the messages this browser holds; older ones may only be on the phone. If WhatsApp Web is open in another tab of the same browser, the run stops and asks to close that tab.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/search_messages`
- Updated: 2026-10-13 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/search_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/search_messages
```

## Input

- `query` (string, required): Words to search for in message text.
- `page` (integer, optional): Page of results, newest first. Ask the next page while `complete` is false.
- `count` (integer, optional): Results per page.
- `chatId` (string, optional): Search inside this chat only, as get_inbox returns it in `chatId`. Omit to search every chat.

## Output

- `complete` (boolean, required): True when no further page exists.
- `messages` (array, required): Matching messages, newest first.

## FAQ

### What does "Search WhatsApp messages" do?

Search WhatsApp messages by words, in every chat or inside one chat given by its `chatId` from get_inbox. Returns the matching messages, newest first, each with its id, chat, sender (in groups), time and text, so a hit feeds get_conversation and the message scripts. Results come in pages: ask the next page while `complete` is false. A page can hold fewer results than asked. An empty list means nothing matched. Searching opens no chat and marks nothing as read. The search covers the messages this browser holds; older ones may only be on the phone. If WhatsApp Web is open in another tab of the same browser, the run stops and asks to close that tab.

### How do I automatically search WhatsApp messages on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/search_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/search_messages

### Is there a web.whatsapp.com API to search WhatsApp messages?

You do not need one. "Search WhatsApp messages" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, count, chatId.

### What does it return?

It returns complete, messages.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/search_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/search_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/search_messages
