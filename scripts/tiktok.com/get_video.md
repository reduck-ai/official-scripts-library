# Get TikTok video

Automatically get TikTok video on tiktok.com. Get a TikTok video's caption, stats, author, music, hashtags and metadata by URL or video id.

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_video`
- Updated: 2026-09-08 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_video`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_video
```

## Input

- `video` (string, required): Full TikTok video URL (https://www.tiktok.com/@user/video/123...) or a bare numeric video id.

## Output

- `id` (string, required)
- `desc` (string, required): Caption text.
- `stats` (object, required)
- `author` (object, required)
- `createTime` (integer, required): Unix seconds.
- `music` (object | null, optional)
- `video` (object, optional)
- `hashtags` (array, optional)
- `mentions` (array, optional): Mentioned @usernames.
- `locationCreated` (string | null, optional): ISO country code where the video was created.

## FAQ

### What does "Get TikTok video" do?

Get a TikTok video's caption, stats, author, music, hashtags and metadata by URL or video id.

### How do I automatically get TikTok video on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_video

### Is there a tiktok.com API to get TikTok video?

You do not need one. "Get TikTok video" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: video.

### What does it return?

It returns id, desc, music, stats, video, author, hashtags, mentions, createTime, locationCreated.

### Do I need to be logged in to tiktok.com?

No. It only uses pages of tiktok.com that are reachable without signing in.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_video

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_video
