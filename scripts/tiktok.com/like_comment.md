# Like TikTok Comment

Automatically like TikTok Comment on tiktok.com. Likes a top-level comment on a public TikTok video, matched by its exact text. Idempotent — already-liked comments are reported, not re-liked.

- Site: tiktok.com
- Address: `reduck/tiktok.com/like_comment`
- Updated: 2026-09-10 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/like_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/like_comment
```

## Input

- `videoUrl` (string, required): The video's canonical URL, e.g. https://www.tiktok.com/@someuser/video/1234567890123456789.
- `commentText` (string, required): The exact, full text of the top-level comment to like, as it appears on the video. Comments have no visible ID in the UI, so text is the only handle a caller can read off the page — it must match exactly (including emoji), and must be unique among top-level comments on the video.

## Output

- `liked` (boolean, required)
- `video_url` (string, required)
- `comment_text` (string, required)
- `already_liked` (boolean, required)

## FAQ

### What does "Like TikTok Comment" do?

Likes a top-level comment on a public TikTok video, matched by its exact text. Idempotent — already-liked comments are reported, not re-liked.

### How do I automatically like TikTok Comment on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/like_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/like_comment

### Is there a tiktok.com API to like TikTok Comment?

You do not need one. "Like TikTok Comment" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: videoUrl, commentText.

### What does it return?

It returns liked, video_url, comment_text, already_liked.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/like_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/like_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/like_comment
