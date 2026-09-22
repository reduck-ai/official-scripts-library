# Download TikTok video (mp4)

Automatically download TikTok video (mp4) on tiktok.com. Download a TikTok video's mp4 bytes by URL or id, returned as base64 (caller decodes to a file). Pick a quality to control size.

- Site: tiktok.com
- Address: `reduck/tiktok.com/download_video`
- Updated: 2026-09-08 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/download_video`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/download_video
```

## Input

- `video` (string, required): Full TikTok video URL or a bare numeric video id.
- `quality` (string, optional): Which encoded rendition to fetch, by ascending bitrate. base64 inflates size ~33%, so prefer lower for large/long videos (see sizeBytes in the output).

## Output

- `mime` (string, required)
- `base64` (string, required): Base64-encoded mp4 bytes. Decode and write to a .mp4 file.
- `videoId` (string, required)
- `sizeBytes` (integer, required): Decoded mp4 size in bytes.
- `quality` (string, optional)
- `gearName` (string | null, optional): TikTok's internal rendition label for the chosen quality.

## FAQ

### What does "Download TikTok video (mp4)" do?

Download a TikTok video's mp4 bytes by URL or id, returned as base64 (caller decodes to a file). Pick a quality to control size.

### How do I automatically download TikTok video (mp4) on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/download_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/download_video

### Is there a tiktok.com API to download TikTok video (mp4)?

You do not need one. "Download TikTok video (mp4)" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: video. Optional: quality.

### What does it return?

It returns mime, base64, quality, videoId, gearName, sizeBytes.

### Do I need to be logged in to tiktok.com?

No. It only uses pages of tiktok.com that are reachable without signing in.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/download_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/download_video

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/download_video
