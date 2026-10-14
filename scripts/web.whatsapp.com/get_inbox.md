# Get WhatsApp inbox

Automatically get WhatsApp inbox on web.whatsapp.com. List the chats of the WhatsApp chat list, in the order the list shows them, most recent first. Pick the same tab as the app: all chats, unread, favorites, groups, or archived. Each chat gives its id, its name, when it was last active, its unread count, whether it is pinned, muted, a favorite or marked unread by hand, and its last message with id, type, sender, time and text. `total` tells how many chats the tab holds, so a result cut by `count` is visible. Reading the list does not open a chat and marks nothing as read. If WhatsApp Web is open in another tab of the same browser, the run stops and asks to close that tab, because taking the session would disconnect it. If the browser is not linked to WhatsApp, the run stops and says so.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/get_inbox`
- Updated: 2026-10-13 (v12)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/get_inbox`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_inbox
```

## Input

- `count` (integer, optional): Maximum number of chats to return, from the top of the list.
- `filter` (string, optional): Which list to read, as the chat list's own tabs: all chats, unread ones, favorites, groups, or the archived chats.

## Output

- `chats` (array, required): Chats in the order the list shows them, most recent first.
- `total` (integer, required): How many chats the list holds for this filter. More than the number returned means count cut the list.

## FAQ

### What does "Get WhatsApp inbox" do?

List the chats of the WhatsApp chat list, in the order the list shows them, most recent first. Pick the same tab as the app: all chats, unread, favorites, groups, or archived. Each chat gives its id, its name, when it was last active, its unread count, whether it is pinned, muted, a favorite or marked unread by hand, and its last message with id, type, sender, time and text. `total` tells how many chats the tab holds, so a result cut by `count` is visible. Reading the list does not open a chat and marks nothing as read. If WhatsApp Web is open in another tab of the same browser, the run stops and asks to close that tab, because taking the session would disconnect it. If the browser is not linked to WhatsApp, the run stops and says so.

### How do I automatically get WhatsApp inbox on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_inbox

### Is there a web.whatsapp.com API to get WhatsApp inbox?

You do not need one. "Get WhatsApp inbox" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Optional: count, filter.

### What does it return?

It returns chats, total.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_inbox

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/get_inbox
