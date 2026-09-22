# WhatsApp — Download media

Automatically download media on web.whatsapp.com. Download the media of a WhatsApp message (image, document, audio/voice) by chat name + message id (the `id` from get_conversation / search_messages), returned as base64 plus filename, mimeType and size. Documents come back byte-for-byte — a file sent by send_message round-trips identically — and carry the filename WhatsApp itself saves them under. Images are read from the inline blob, which is WhatsApp's own rendition and may be smaller than a large original, so imageWidth/Height are reported rather than implying full fidelity. Audio/voice notes use the same path as documents but are unverified for lack of a fixture. Video, sticker, GIF and location messages are not supported: they are refused with their actual kind named, so check a message's `media` field from get_conversation if you are unsure what it holds.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/download_media`
- Updated: 2026-09-09 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/download_media`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/download_media
```

## Input

- `id` (string, required): WhatsApp message id - the data-id from send_media's messageId, or from get_conversation/search_messages. The message must be an image or a document/audio (voice note) message: video, sticker, GIF and location messages carry no supported file and are refused with their actual kind named. Check the message's `media` field from get_conversation first if you are unsure.
- `name` (string, required): Exact chat/contact/group name containing the message (the name field from get_inbox).

## Output

- `size` (integer, required): Byte size of the returned media.
- `base64` (string, required)
- `filename` (string, required)
- `mimeType` (string, required)
- `kind` (string, optional)
- `imageWidth` (integer | null, optional): Natural width of the rendition returned. For a large photo WhatsApp's inline blob can be smaller than the original upload.
- `imageHeight` (integer | null, optional)

## FAQ

### What does "WhatsApp — Download media" do?

Download the media of a WhatsApp message (image, document, audio/voice) by chat name + message id (the `id` from get_conversation / search_messages), returned as base64 plus filename, mimeType and size. Documents come back byte-for-byte — a file sent by send_message round-trips identically — and carry the filename WhatsApp itself saves them under. Images are read from the inline blob, which is WhatsApp's own rendition and may be smaller than a large original, so imageWidth/Height are reported rather than implying full fidelity. Audio/voice notes use the same path as documents but are unverified for lack of a fixture. Video, sticker, GIF and location messages are not supported: they are refused with their actual kind named, so check a message's `media` field from get_conversation if you are unsure what it holds.

### How do I automatically download media on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/download_media, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/download_media

### Is there a web.whatsapp.com API to download media?

You do not need one. "WhatsApp — Download media" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name, id.

### What does it return?

It returns kind, size, base64, filename, mimeType, imageWidth, imageHeight.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/download_media, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/download_media

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/download_media
