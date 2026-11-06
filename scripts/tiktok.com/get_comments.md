# Get TikTok video comments

Automatically get TikTok video comments on tiktok.com. List the top-level comments on a TikTok video, given its URL or id, one page at a time in TikTok's order, with the total count. Pass the returned cursor to get the next page; cursor is null on the last page. A video id that does not exist is an error.

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_comments`
- Updated: 2026-11-05 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_comments`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_comments
```

## Input

- `video` (string, required): Full TikTok video URL or a bare numeric video id.
- `count` (integer, optional): How many top-level comments to ask TikTok for on this page.
- `cursor` (integer, optional): Where the page starts: 0 for the first page, then the cursor a previous run returned.

## Output

- `total` (integer, required): Total comment count reported by TikTok.
- `cursor` (integer | null, required): Pass as cursor for the next page; null when there is none.
- `hasMore` (boolean, required)
- `videoId` (string, required)
- `comments` (array, required)

## FAQ

### What does "Get TikTok video comments" do?

List the top-level comments on a TikTok video, given its URL or id, one page at a time in TikTok's order, with the total count. Pass the returned cursor to get the next page; cursor is null on the last page. A video id that does not exist is an error.

### How do I automatically get TikTok video comments on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_comments

### Is there a tiktok.com API to get TikTok video comments?

You do not need one. "Get TikTok video comments" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: video. Optional: count, cursor.

### What does it return?

It returns total, cursor, hasMore, videoId, comments.

### Do I need to be logged in to tiktok.com?

No. It only uses pages of tiktok.com that are reachable without signing in.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_comments

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_comments
