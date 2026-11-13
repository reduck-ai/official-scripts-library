# Download a Telegram message's file

Automatically download a Telegram message's file on web.telegram.org. Download the file of one Telegram message (photo, video, document, audio, voice note or sticker) as base64, with its name, type and size. Takes a peer id or a public @username, and the message id from get_conversation or search_messages. Photos come at their largest size. Refuses a message without a file, and a file larger than 6 MB. Does not mark the conversation as read.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/download_media`
- Updated: 2026-11-12 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/download_media`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/download_media
```

## Input

- `peerId` (string, required): The conversation: its peerId from web.telegram.org/get_inbox, or a public @username (such as "@telegram").
- `messageId` (string, required): The message carrying the file, as web.telegram.org/get_conversation or search_messages return it.

## Output

- `kind` (string, required): photo, video, document, audio, voice, sticker or videoNote.
- `base64` (string, required): The file's bytes, base64-encoded. Documents come back as sent; photos as Telegram stores them (the largest size).
- `peerId` (string, required)
- `fileName` (string, required): The file's own name for a document, audio or video; for a photo, voice note or sticker, which have none, the media id with its extension.
- `messageId` (string, required)
- `byteLength` (integer, required)
- `mimeType` (string | null, optional)

## FAQ

### What does "Download a Telegram message's file" do?

Download the file of one Telegram message (photo, video, document, audio, voice note or sticker) as base64, with its name, type and size. Takes a peer id or a public @username, and the message id from get_conversation or search_messages. Photos come at their largest size. Refuses a message without a file, and a file larger than 6 MB. Does not mark the conversation as read.

### How do I automatically download a Telegram message's file on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/download_media, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/download_media

### Is there a web.telegram.org API to download a Telegram message's file?

You do not need one. "Download a Telegram message's file" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Required: peerId, messageId.

### What does it return?

It returns kind, base64, peerId, fileName, mimeType, messageId, byteLength.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It only reads. It looks things up on web.telegram.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/download_media, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/download_media

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/download_media
