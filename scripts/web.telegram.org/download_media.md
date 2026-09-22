# Telegram — Download a message's media

Automatically download a message's media on web.telegram.org. Pull the bytes of a document, photo or video attached to a Telegram message, given its conversation peer id and message id, returned as base64 plus the filename Telegram stores it under. Drives the message's own Download action and reads the file out of the app rather than relying on a browser download, and refuses a message that carries no media. Two side effects worth knowing: opening the conversation marks it read, and Telegram also saves the file to the browser's download folder. Note that photos are Telegram's re-encoded JPEG, not the original upload; documents come back byte-for-byte.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/download_media`
- Updated: 2026-08-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/download_media`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/download_media
```

## Input

- `peerId` (string, required): The conversation's peer id, as returned by get_inbox (e.g. "8591421602" for Saved Messages; negative ids are channels and groups).
- `messageId` (string, required): The message carrying the media, as returned by get_conversation or send_message. Must be one of the recently loaded messages in that conversation — get_conversation only loads a recent window, so raise its count until the target is present.

## Output

- `kind` (string, required): Which bubble shape it was read from: "document" for a file bubble (a filename and size are shown in the chat), "media" for a photo or video bubble.
- `base64` (string, required): The file's bytes, base64-encoded — the exact inverse of send_message's fileBase64, so a file can be round-tripped between conversations. Documents come back byte-for-byte identical to what was sent.
- `peerId` (string, required): The peer id that was actually opened, read back from the address bar.
- `filename` (string, required): The name Telegram saves the file under, taken from its own download action rather than guessed. For a document this is the original filename; for a photo it is Telegram's generated name (e.g. "5793955541833946033.jpg").
- `messageId` (string, required): The message the media came from.
- `byteLength` (integer, required): Size of the returned bytes. For a document this matches the size shown on the bubble; for a photo it is the size of Telegram's re-encoded copy, which will not match the original upload.
- `verified_on_page` (boolean, required): True when the bytes were actually captured from the app's own download action, rather than the click being assumed to have worked.
- `mimeType` (string | null, optional): The MIME type Telegram attached to the blob it saved, or null if it did not set one.
- `chatTitle` (string | null, optional): The conversation title from the header — echo this to a human, since a peer id is not recognisable.

## FAQ

### What does "Telegram — Download a message's media" do?

Pull the bytes of a document, photo or video attached to a Telegram message, given its conversation peer id and message id, returned as base64 plus the filename Telegram stores it under. Drives the message's own Download action and reads the file out of the app rather than relying on a browser download, and refuses a message that carries no media. Two side effects worth knowing: opening the conversation marks it read, and Telegram also saves the file to the browser's download folder. Note that photos are Telegram's re-encoded JPEG, not the original upload; documents come back byte-for-byte.

### How do I automatically download a message's media on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/download_media, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/download_media

### Is there a web.telegram.org API to download a message's media?

You do not need one. "Telegram — Download a message's media" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Required: peerId, messageId.

### What does it return?

It returns kind, base64, peerId, filename, mimeType, chatTitle, messageId, byteLength, verified_on_page.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It only reads. It looks things up on web.telegram.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/download_media, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/download_media

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/download_media
