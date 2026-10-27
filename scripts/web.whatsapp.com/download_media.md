# WhatsApp — Download media

Automatically download media on web.whatsapp.com. Download the file of one WhatsApp message (image, video, document, audio, voice note or sticker) to the computer running the browser, and return where it was saved: path (or url when the file is not on that computer), file name, type, size and, for images and videos, the width and height WhatsApp states. Give the message by its id from get_conversation; a bare key id also works with the chat's name. The file is checked byte for byte against WhatsApp's own fingerprint before it is saved. The chat is not opened, so nothing is marked as read. A message deleted for everyone, or one with no file (text, location), is refused with its kind named. If the browser is not linked to WhatsApp, or WhatsApp Web is open in another tab of the same browser, the run stops and says so.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/download_media`
- Updated: 2026-10-23 (v15)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/download_media`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/download_media
```

## Input

- `id` (string, required): The message id, as get_conversation returns it in `id` (false_<chat>_<key> or true_<chat>_<key>). A bare key id (the last part alone) also works when `name` is given.
- `name` (string, optional): The chat's name as get_inbox returns it. Needed only when `id` is a bare key id.

## Output

- `kind` (string, required): WhatsApp's message type: image, video, document, audio, ptt (voice note) or sticker.
- `size` (integer, required): Size of the saved file in bytes.
- `chatId` (string, required): The chat the message belongs to, as get_inbox returns it in `chatId`.
- `filename` (string, required): Name of the saved file. A document keeps the name it was sent with; it can carry a numbered suffix when a file of that name was already there.
- `mimeType` (string, required)
- `messageId` (string, required)
- `url` (string | null, optional): A link to the file, when it is not saved on the computer running the browser.
- `path` (string | null, optional): Where the file was saved on the computer running the browser.
- `imageWidth` (integer | null, optional): Width WhatsApp states for an image, video or sticker; null otherwise.
- `imageHeight` (integer | null, optional)

## FAQ

### What does "WhatsApp — Download media" do?

Download the file of one WhatsApp message (image, video, document, audio, voice note or sticker) to the computer running the browser, and return where it was saved: path (or url when the file is not on that computer), file name, type, size and, for images and videos, the width and height WhatsApp states. Give the message by its id from get_conversation; a bare key id also works with the chat's name. The file is checked byte for byte against WhatsApp's own fingerprint before it is saved. The chat is not opened, so nothing is marked as read. A message deleted for everyone, or one with no file (text, location), is refused with its kind named. If the browser is not linked to WhatsApp, or WhatsApp Web is open in another tab of the same browser, the run stops and says so.

### How do I automatically download media on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/download_media, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/download_media

### Is there a web.whatsapp.com API to download media?

You do not need one. "WhatsApp — Download media" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: id. Optional: name.

### What does it return?

It returns url, kind, path, size, chatId, filename, mimeType, messageId, imageWidth, imageHeight.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/download_media, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/download_media

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/download_media
