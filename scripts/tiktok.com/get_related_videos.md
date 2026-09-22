# Get TikTok related videos

Automatically get TikTok related videos on tiktok.com. Get the “you may like” related-video recommendations shown next to a TikTok video (a single ~12-item snapshot, not a paginable list).

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_related_videos`
- Updated: 2026-09-08 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_related_videos`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_related_videos
```

## Input

- `video` (string, required): Full TikTok video URL or a bare numeric video id.

## Output

- `videos` (array, required): The recommendation batch the video page loads (~12 items). This is a non-deterministic snapshot: TikTok re-ranks it per load, so it is not stably paginable.
- `videoId` (string, required)

## FAQ

### What does "Get TikTok related videos" do?

Get the “you may like” related-video recommendations shown next to a TikTok video (a single ~12-item snapshot, not a paginable list).

### How do I automatically get TikTok related videos on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_related_videos, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_related_videos

### Is there a tiktok.com API to get TikTok related videos?

You do not need one. "Get TikTok related videos" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: video.

### What does it return?

It returns videos, videoId.

### Do I need to be logged in to tiktok.com?

No. It only uses pages of tiktok.com that are reachable without signing in.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_related_videos, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_related_videos

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_related_videos
