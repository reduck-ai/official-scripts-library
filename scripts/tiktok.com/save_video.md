# Save (Favourite) TikTok Video

Automatically save (Favourite) TikTok Video on tiktok.com. Adds a public TikTok video to this account's Favourites. Idempotent — already-saved videos are reported, not re-saved.

- Site: tiktok.com
- Address: `reduck/tiktok.com/save_video`
- Updated: 2026-09-10 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/save_video`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/save_video
```

## Input

- `videoUrl` (string, required): The video's canonical URL, e.g. https://www.tiktok.com/@someuser/video/1234567890123456789 — the format TikTok itself uses for sharing and that appears when you open a video from a profile grid.

## Output

- `saved` (boolean, required)
- `video_url` (string, required)
- `already_saved` (boolean, required)

## FAQ

### What does "Save (Favourite) TikTok Video" do?

Adds a public TikTok video to this account's Favourites. Idempotent — already-saved videos are reported, not re-saved.

### How do I automatically save (Favourite) TikTok Video on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/save_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/save_video

### Is there a tiktok.com API to save (Favourite) TikTok Video?

You do not need one. "Save (Favourite) TikTok Video" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: videoUrl.

### What does it return?

It returns saved, video_url, already_saved.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/save_video, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/save_video

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/save_video
