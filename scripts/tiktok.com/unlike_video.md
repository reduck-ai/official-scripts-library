# Unlike a TikTok video

Automatically unlike a TikTok video on tiktok.com. Remove your like from a TikTok video (as the logged-in account) by URL or id. Safe to repeat: it does nothing if you haven't liked it.

- Site: tiktok.com
- Address: `reduck/tiktok.com/unlike_video`
- Updated: 2026-08-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/unlike_video`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/unlike_video
```

## Input

- `video` (string, required): Full TikTok video URL or a bare numeric video id.

## Output

- `liked` (boolean, required): Like state after the call (false once unliked).
- `changed` (boolean, required): True if this call flipped the state; false if it was already not liked.
- `videoId` (string, required)

## FAQ

### What does "Unlike a TikTok video" do?

Remove your like from a TikTok video (as the logged-in account) by URL or id. Safe to repeat: it does nothing if you haven't liked it.

### How do I automatically unlike a TikTok video on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/unlike_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/unlike_video

### Is there a tiktok.com API to unlike a TikTok video?

You do not need one. "Unlike a TikTok video" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: video.

### What does it return?

It returns liked, changed, videoId.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/unlike_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/unlike_video

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/unlike_video
