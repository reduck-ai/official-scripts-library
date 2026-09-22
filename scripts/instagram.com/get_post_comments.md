# Get Instagram post comments

Automatically get Instagram post comments on instagram.com. Fetch the preview comments of an Instagram post or reel by shortcode, plus its caption and counts. Returns code, url, caption, comments (text, user, verified, created_at, like_count, reply_count), like_count, view_count, comment_count, and comments_disabled. Only returns the comments Instagram renders by default, not the full thread, capped to count.

- Site: instagram.com
- Address: `reduck/instagram.com/get_post_comments`
- Updated: 2026-09-03 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_post_comments`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_post_comments
```

## Input

- `code` (string, required): Post shortcode, e.g. the X in instagram.com/p/X/
- `count` (integer, optional): Max comments to return

## Output

- `code` (string, required)
- `comments` (array, required)
- `url` (string, optional)
- `caption` (string | null, optional)
- `like_count` (integer | null, optional)
- `view_count` (integer | null, optional)
- `comment_count` (integer | null, optional)
- `comments_disabled` (boolean, optional)

## FAQ

### What does "Get Instagram post comments" do?

Fetch the preview comments of an Instagram post or reel by shortcode, plus its caption and counts. Returns code, url, caption, comments (text, user, verified, created_at, like_count, reply_count), like_count, view_count, comment_count, and comments_disabled. Only returns the comments Instagram renders by default, not the full thread, capped to count.

### How do I automatically get Instagram post comments on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_post_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_post_comments

### Is there a instagram.com API to get Instagram post comments?

You do not need one. "Get Instagram post comments" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: code. Optional: count.

### What does it return?

It returns url, code, caption, comments, like_count, view_count, comment_count, comments_disabled.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_post_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_post_comments

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_post_comments
