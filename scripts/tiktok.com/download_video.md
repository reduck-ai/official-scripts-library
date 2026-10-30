# Download TikTok video (mp4)

Automatically download TikTok video (mp4) on tiktok.com. Download a TikTok video as an mp4 file by URL or id. Returns the saved file's name, its path on your own Chrome (or a link on a managed browser) and its size. Pick a quality to control size. An unknown, deleted or private video fails with a message to check the URL or id.

- Site: tiktok.com
- Address: `reduck/tiktok.com/download_video`
- Updated: 2026-10-29 (v5)
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
- `videoId` (string, required)
- `filename` (string, required): Saved file name (can end in " (2)").
- `sizeBytes` (integer, required): Size of the mp4 in bytes.
- `url` (string | null, optional): Link to the saved mp4 (managed browser).
- `path` (string | null, optional): Where the mp4 was saved on the machine running the browser (your own Chrome).
- `quality` (string, optional)
- `gearName` (string | null, optional): TikTok's own label for the chosen rendition.

## FAQ

### What does "Download TikTok video (mp4)" do?

Download a TikTok video as an mp4 file by URL or id. Returns the saved file's name, its path on your own Chrome (or a link on a managed browser) and its size. Pick a quality to control size. An unknown, deleted or private video fails with a message to check the URL or id.

### How do I automatically download TikTok video (mp4) on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/download_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/download_video

### Is there a tiktok.com API to download TikTok video (mp4)?

You do not need one. "Download TikTok video (mp4)" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: video. Optional: quality.

### What does it return?

It returns url, mime, path, quality, videoId, filename, gearName, sizeBytes.

### Do I need to be logged in to tiktok.com?

No. It only uses pages of tiktok.com that are reachable without signing in.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/download_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/download_video

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/download_video
