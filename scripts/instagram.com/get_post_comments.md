# Get Instagram post comments

Automatically get Instagram post comments on instagram.com. Fetch the top-level comments of an Instagram post or reel by its shortcode or link, in Instagram's own order, plus its caption and counts. Returns code, url, caption, comments (id, text, user, verified, created_at, like_count, reply_count), like_count, view_count, comment_count (Instagram's count, replies included), comments_disabled and complete. Reads up to count comments (default 12); complete is true only when every top-level comment was read, false when count stopped the list first. Replies are not included. A post with no comments returns an empty list. A post that was removed, is private to this account, or a wrong code fails with an error that says so.

- Site: instagram.com
- Address: `reduck/instagram.com/get_post_comments`
- Updated: 2026-11-11 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_post_comments`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_post_comments
```

## Input

- `code` (string, required): The post's shortcode, the X in instagram.com/p/X/ or instagram.com/reel/X/, or that whole link. instagram.com/get_user_posts returns it as code.
- `count` (integer, optional): Maximum number of top-level comments to return.

## Output

- `code` (string, required)
- `comments` (array, required)
- `complete` (boolean, required): True when every top-level comment was read; false when count stopped the list first.
- `url` (string, optional)
- `caption` (string | null, optional)
- `like_count` (integer | null, optional)
- `view_count` (integer | null, optional)
- `comment_count` (integer | null, optional): Instagram's own count, replies included, so it can exceed the number of top-level comments.
- `comments_disabled` (boolean, optional)

## FAQ

### What does "Get Instagram post comments" do?

Fetch the top-level comments of an Instagram post or reel by its shortcode or link, in Instagram's own order, plus its caption and counts. Returns code, url, caption, comments (id, text, user, verified, created_at, like_count, reply_count), like_count, view_count, comment_count (Instagram's count, replies included), comments_disabled and complete. Reads up to count comments (default 12); complete is true only when every top-level comment was read, false when count stopped the list first. Replies are not included. A post with no comments returns an empty list. A post that was removed, is private to this account, or a wrong code fails with an error that says so.

### How do I automatically get Instagram post comments on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_post_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_post_comments

### Is there a instagram.com API to get Instagram post comments?

You do not need one. "Get Instagram post comments" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: code. Optional: count.

### What does it return?

It returns url, code, caption, comments, complete, like_count, view_count, comment_count, comments_disabled.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_post_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_post_comments

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_post_comments
