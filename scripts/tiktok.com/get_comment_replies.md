# Get TikTok comment replies

Automatically get TikTok comment replies on tiktok.com. List the replies to a TikTok comment, given the parent comment id and the video id.

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_comment_replies`
- Updated: 2026-09-08 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_comment_replies`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_comment_replies
```

## Input

- `video` (string, required): Full TikTok video URL or bare video id (the item the comment belongs to).
- `commentId` (string, required): Parent comment id (the `id` field returned by get_comments).
- `count` (integer, optional): Target number of replies to collect.

## Output

- `total` (integer, required): Total replies reported by TikTok.
- `hasMore` (boolean, required)
- `replies` (array, required)
- `videoId` (string, required)
- `commentId` (string, required)

## FAQ

### What does "Get TikTok comment replies" do?

List the replies to a TikTok comment, given the parent comment id and the video id.

### How do I automatically get TikTok comment replies on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_comment_replies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_comment_replies

### Is there a tiktok.com API to get TikTok comment replies?

You do not need one. "Get TikTok comment replies" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: video, commentId. Optional: count.

### What does it return?

It returns total, hasMore, replies, videoId, commentId.

### Do I need to be logged in to tiktok.com?

No. It only uses pages of tiktok.com that are reachable without signing in.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_comment_replies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_comment_replies

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_comment_replies
