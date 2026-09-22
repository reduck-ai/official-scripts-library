# Get Instagram DM attachment

Automatically get Instagram DM attachment on instagram.com. Download the media attached to an Instagram DM message (photo, video, clip/reel share, voice note) by thread_id plus message id. Returns filename, mimeType, size and the bytes as base64, plus the direct media URL. Omit the message id to take the most recent media in the thread.

- Site: instagram.com
- Address: `reduck/instagram.com/get_dm_attachment`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_dm_attachment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_dm_attachment
```

## Input

- `threadId` (string, required): Instagram DM thread id (thread_id from instagram.com/get_inbox).
- `maxBytes` (integer, optional): Refuse to base64-encode anything larger than this. Default 8000000 (8 MB) — videos can be far bigger, and the URL is still returned so it can be fetched directly.
- `messageId` (string, optional): Message/item id to download. Omit to take the most recent message in the thread that carries media.

## Output

- `itemType` (string, required): Instagram's item_type, e.g. media, clip, voice_media, animated_media, media_share.
- `mediaUrl` (string, required)
- `threadId` (string, required)
- `messageId` (string, required)
- `size` (integer | null, optional): Byte size of the downloaded media.
- `base64` (string | null, optional): Media bytes, base64-encoded. Null when the media exceeded maxBytes — mediaUrl is still usable.
- `filename` (string | null, optional)
- `mimeType` (string | null, optional)
- `pickedLatest` (boolean, optional): True when no messageId was given and the newest media item was used.
- `skippedEncoding` (boolean, optional): True when the bytes were not encoded because they exceeded maxBytes.

## FAQ

### What does "Get Instagram DM attachment" do?

Download the media attached to an Instagram DM message (photo, video, clip/reel share, voice note) by thread_id plus message id. Returns filename, mimeType, size and the bytes as base64, plus the direct media URL. Omit the message id to take the most recent media in the thread.

### How do I automatically get Instagram DM attachment on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_dm_attachment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_dm_attachment

### Is there a instagram.com API to get Instagram DM attachment?

You do not need one. "Get Instagram DM attachment" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: threadId. Optional: maxBytes, messageId.

### What does it return?

It returns size, base64, filename, itemType, mediaUrl, mimeType, threadId, messageId, pickedLatest, skippedEncoding.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_dm_attachment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_dm_attachment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_dm_attachment
