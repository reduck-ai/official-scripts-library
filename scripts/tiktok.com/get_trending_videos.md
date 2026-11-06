# Get TikTok trending videos

Automatically get TikTok trending videos on tiktok.com. Get one snapshot of TikTok's Explore (trending) feed, optionally for one Explore category. TikTok re-ranks the feed on every request and can return fewer videos than asked; run again for another snapshot. An unknown category is an error.

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_trending_videos`
- Updated: 2026-11-05 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_trending_videos`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_trending_videos
```

## Input

- `count` (integer, optional): How many trending videos to ask TikTok for.
- `categoryType` (integer, optional): Explore category id (120 = all trending; other numeric ids map to the Explore category tabs). Category 0 is invalid.

## Output

- `videos` (array, required): A re-ranked trending snapshot (order not stable across runs).

## FAQ

### What does "Get TikTok trending videos" do?

Get one snapshot of TikTok's Explore (trending) feed, optionally for one Explore category. TikTok re-ranks the feed on every request and can return fewer videos than asked; run again for another snapshot. An unknown category is an error.

### How do I automatically get TikTok trending videos on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_trending_videos, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_trending_videos

### Is there a tiktok.com API to get TikTok trending videos?

You do not need one. "Get TikTok trending videos" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Optional: count, categoryType.

### What does it return?

It returns videos.

### Do I need to be logged in to tiktok.com?

No. It only uses pages of tiktok.com that are reachable without signing in.

### Does it change anything on tiktok.com, or only read data?

Unknown: its author has not declared whether it changes anything on tiktok.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_trending_videos, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_trending_videos

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_trending_videos
