# Get TikTok comment replies

Automatically get TikTok comment replies on tiktok.com. List one page of replies to a TikTok comment, given the parent comment id and the video. Returns TikTok's total reply count, hasMore, and a nextCursor to pass back as cursor for the next page.

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_comment_replies`
- Updated: 2026-11-04 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_comment_replies`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_comment_replies
```

## Input

- `video` (string, required): Full TikTok video URL or bare video id (the item the comment belongs to).
- `commentId` (string, required): Parent comment id (the `id` field returned by get_comments).
- `count` (integer, optional): How many replies to ask TikTok for in this page.
- `cursor` (integer, optional): Where to start: 0 for the first page, then the nextCursor of the previous call.

## Output

- `total` (integer, required): Total replies reported by TikTok.
- `hasMore` (boolean, required)
- `replies` (array, required)
- `videoId` (string, required)
- `commentId` (string, required)
- `nextCursor` (integer | null, optional): Pass as cursor to get the next page; null when there is none.

## FAQ

### What does "Get TikTok comment replies" do?

List one page of replies to a TikTok comment, given the parent comment id and the video. Returns TikTok's total reply count, hasMore, and a nextCursor to pass back as cursor for the next page.

### How do I automatically get TikTok comment replies on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_comment_replies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_comment_replies

### Is there a tiktok.com API to get TikTok comment replies?

You do not need one. "Get TikTok comment replies" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: video, commentId. Optional: count, cursor.

### What does it return?

It returns total, hasMore, replies, videoId, commentId, nextCursor.

### Do I need to be logged in to tiktok.com?

No. It only uses pages of tiktok.com that are reachable without signing in.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_comment_replies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_comment_replies

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_comment_replies
