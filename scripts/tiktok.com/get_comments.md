# Get TikTok video comments

Automatically get TikTok video comments on tiktok.com. List the top-level comments on a TikTok video, given its URL or id, in newest-relevance order.

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_comments`
- Updated: 2026-09-08 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_comments`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_comments
```

## Input

- `video` (string, required): Full TikTok video URL or a bare numeric video id.
- `count` (integer, optional): Target number of top-level comments. Resuming by cursor is impossible (TikTok signs each request); the script scrolls from the top each run.

## Output

- `total` (integer, required): Total comment count reported by TikTok.
- `hasMore` (boolean, required)
- `videoId` (string, required)
- `comments` (array, required)

## FAQ

### What does "Get TikTok video comments" do?

List the top-level comments on a TikTok video, given its URL or id, in newest-relevance order.

### How do I automatically get TikTok video comments on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_comments

### Is there a tiktok.com API to get TikTok video comments?

You do not need one. "Get TikTok video comments" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: video. Optional: count.

### What does it return?

It returns total, hasMore, videoId, comments.

### Do I need to be logged in to tiktok.com?

No. It only uses pages of tiktok.com that are reachable without signing in.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_comments

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_comments
