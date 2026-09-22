# WhatsApp — List a chat's media, documents or links

Automatically list a chat's media, documents or links on web.whatsapp.com. List what has been shared in one WhatsApp chat, from the chat's own media, links and documents gallery — pick which view you want with `tab`. Documents come back with the message id, filename, size, caption and time, so they can be fed straight to download_media. Images and videos are the exception: the gallery does not expose an identifiable handle for them, so those entries return only WhatsApp's own accessible label — use get_conversation when you need to act on a specific photo or video. Links come back with the URL, its preview title and the surrounding message. Reaches further back than the conversation view, whose scrollback is bounded.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/get_chat_media`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/get_chat_media`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_chat_media
```

## Input

- `name` (string, required): Exact chat/contact/group name whose gallery to read (the `name` field from get_inbox).
- `tab` (string, optional): Which view of the gallery to read — these are the three tabs WhatsApp itself offers. One call reads one tab; loop if you need all three.
- `count` (integer, optional): Maximum entries to return, scrolling the gallery to load older ones.

## Output

- `tab` (string, required): Which tab was read.
- `chat` (string, required): The chat whose gallery was read, confirmed from the conversation header.
- `count` (integer, required): How many entries were returned.
- `items` (array, required): The gallery entries, newest first. Empty when the tab has nothing in it, which is a real answer.
- `sectionCount` (integer | null, optional): The combined media + docs + links total WhatsApp prints on the chat-info section, captured before the gallery opened. Compare it against `count` to tell a genuinely empty tab from one that failed to load.

## FAQ

### What does "WhatsApp — List a chat's media, documents or links" do?

List what has been shared in one WhatsApp chat, from the chat's own media, links and documents gallery — pick which view you want with `tab`. Documents come back with the message id, filename, size, caption and time, so they can be fed straight to download_media. Images and videos are the exception: the gallery does not expose an identifiable handle for them, so those entries return only WhatsApp's own accessible label — use get_conversation when you need to act on a specific photo or video. Links come back with the URL, its preview title and the surrounding message. Reaches further back than the conversation view, whose scrollback is bounded.

### How do I automatically list a chat's media, documents or links on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_chat_media, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_chat_media

### Is there a web.whatsapp.com API to list a chat's media, documents or links?

You do not need one. "WhatsApp — List a chat's media, documents or links" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name. Optional: tab, count.

### What does it return?

It returns tab, chat, count, items, sectionCount.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_chat_media, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_chat_media

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/get_chat_media
