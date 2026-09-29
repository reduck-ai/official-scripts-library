# Get TikTok post analytics

Automatically get TikTok post analytics on tiktok.com. Read the TikTok Studio analytics for one of your own posts (video or photo), given its URL or id. Returns views, likes, comments, shares, saves, total play time, average watch time, finish rate, new followers and traffic sources (For You, Follow, Search…). Metrics TikTok hasn't computed yet (it needs more views) come back as null. Read-only. It fails with a clear error if the post isn't on the signed-in account.

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_video_analytics`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_video_analytics`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_video_analytics
```

## Input

- `video` (string, required): URL or numeric id of one of your own TikTok posts (video or photo).

## Output

- `id` (string, required)
- `type` (string, required)
- `views` (number | null, required)
- `url` (string, optional)
- `note` (string, optional)
- `likes` (number | null, optional)
- `saves` (number | null, optional)
- `author` (string | null, optional)
- `shares` (number | null, optional)
- `comments` (number | null, optional)
- `createTime` (string | null, optional)
- `finishRate` (number | null, optional): Share of views watched to the end (0-1).
- `description` (string, optional)
- `searchTerms` (any, optional)
- `newFollowers` (number | null, optional)
- `totalPlayTime` (number | null, optional): Total play time as TikTok reports it.
- `uniqueViewers` (number | null, optional)
- `trafficSources` (array | null, optional)
- `averageWatchTime` (number | null, optional): Average watch time as TikTok reports it.

## FAQ

### What does "Get TikTok post analytics" do?

Read the TikTok Studio analytics for one of your own posts (video or photo), given its URL or id. Returns views, likes, comments, shares, saves, total play time, average watch time, finish rate, new followers and traffic sources (For You, Follow, Search…). Metrics TikTok hasn't computed yet (it needs more views) come back as null. Read-only. It fails with a clear error if the post isn't on the signed-in account.

### How do I automatically get TikTok post analytics on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_video_analytics, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_video_analytics

### Is there a tiktok.com API to get TikTok post analytics?

You do not need one. "Get TikTok post analytics" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: video.

### What does it return?

It returns id, url, note, type, likes, saves, views, author, shares, comments, createTime, finishRate, description, searchTerms, newFollowers, totalPlayTime, uniqueViewers, trafficSources, averageWatchTime.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_video_analytics, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_video_analytics

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_video_analytics
