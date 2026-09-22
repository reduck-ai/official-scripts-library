# Search TikTok videos

Automatically search TikTok videos on tiktok.com. Search TikTok videos by keyword, newest-relevance order, up to `count`.

- Site: tiktok.com
- Address: `reduck/tiktok.com/search_videos`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/search_videos`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/search_videos
```

## Input

- `query` (string, required): Search keyword(s).
- `count` (integer, optional): Target number of videos to collect. The script pages the search feed until this many are gathered or results run out.

## Output

- `query` (string, required)
- `videos` (array, required)
- `hasMore` (boolean, required)

## FAQ

### What does "Search TikTok videos" do?

Search TikTok videos by keyword, newest-relevance order, up to `count`.

### How do I automatically search TikTok videos on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/search_videos, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/search_videos

### Is there a tiktok.com API to search TikTok videos?

You do not need one. "Search TikTok videos" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: count.

### What does it return?

It returns query, videos, hasMore.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

Unknown: its author has not declared whether it changes anything on tiktok.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/search_videos, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/search_videos

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/search_videos
