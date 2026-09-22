# Like a TikTok video

Automatically like a TikTok video on tiktok.com. Like a TikTok video (as the logged-in account) by URL or id. Safe to repeat: it does nothing if you already liked it.

- Site: tiktok.com
- Address: `reduck/tiktok.com/like_video`
- Updated: 2026-09-11 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/like_video`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/like_video
```

## Input

- `video` (string, required): Full TikTok video URL or a bare numeric video id.

## Output

- `liked` (boolean, required): True once the video is in the liked state. A returned result always has this true: a like that does not persist raises an error instead of returning.
- `changed` (boolean, required): True if this call flipped the state; false if the video was already liked before the call.
- `videoId` (string, required)

## FAQ

### What does "Like a TikTok video" do?

Like a TikTok video (as the logged-in account) by URL or id. Safe to repeat: it does nothing if you already liked it.

### How do I automatically like a TikTok video on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/like_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/like_video

### Is there a tiktok.com API to like a TikTok video?

You do not need one. "Like a TikTok video" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: video.

### What does it return?

It returns liked, changed, videoId.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/like_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/like_video

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/like_video
