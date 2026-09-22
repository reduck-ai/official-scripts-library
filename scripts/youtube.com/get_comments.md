# Get YouTube comments

Automatically get YouTube comments on youtube.com. List a YouTube video's top-level comments from a watch URL or video id. Per comment: id, text, author, channelId, authorAvatar, publishedTime, likeCount, replyCount, isVerified, isCreator, pinned. Sort by 'top' (default) or 'newest' and paginate with the returned nextCursor. likeCount and replyCount are YouTube's abbreviated strings (e.g. "255k", "960"), and comments come back empty when they are disabled.

- Site: youtube.com
- Address: `reduck/youtube.com/get_comments`
- Updated: 2026-08-19 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/youtube.com/get_comments`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/youtube.com/get_comments
```

## Input

- `video` (string, required): A YouTube video URL (watch?v=, youtu.be/, /shorts/, /embed/) or a bare 11-char video id.
- `sort` (string, optional): Comment sort order. Ignored when paginating with a cursor (the cursor carries its own order).
- `cursor` (string, optional): Pagination token from a previous call's nextCursor. Omit for the first page.

## Output

- `sort` (string | null, required): Effective sort on the first page; null on cursor pages (the cursor carries its own order).
- `videoId` (string, required)
- `comments` (array, required): Empty when the video's comments are disabled. An unavailable video raises an error instead.
- `nextCursor` (string | null, required): Pass back as cursor for the next page; null on the last page.

## FAQ

### What does "Get YouTube comments" do?

List a YouTube video's top-level comments from a watch URL or video id. Per comment: id, text, author, channelId, authorAvatar, publishedTime, likeCount, replyCount, isVerified, isCreator, pinned. Sort by 'top' (default) or 'newest' and paginate with the returned nextCursor. likeCount and replyCount are YouTube's abbreviated strings (e.g. "255k", "960"), and comments come back empty when they are disabled.

### How do I automatically get YouTube comments on youtube.com?

Ask an AI agent connected to Reduck to run reduck/youtube.com/get_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/get_comments

### Is there a youtube.com API to get YouTube comments?

You do not need one. "Get YouTube comments" drives the real youtube.com pages in a browser, so it works whether or not youtube.com offers an API for this.

### What information do I need to provide?

Required: video. Optional: sort, cursor.

### What does it return?

It returns sort, videoId, comments, nextCursor.

### Do I need to be logged in to youtube.com?

No. It only uses pages of youtube.com that are reachable without signing in.

### Does it change anything on youtube.com, or only read data?

It only reads. It looks things up on youtube.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/youtube.com/get_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/get_comments

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/youtube.com/get_comments
