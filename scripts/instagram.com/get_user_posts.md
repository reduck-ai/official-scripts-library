# Get Instagram user posts

Automatically get Instagram user posts on instagram.com. Fetch the most recent posts from an Instagram user's profile, newest first. Returns code, url, taken_at, media_type, caption, like_count, comment_count, images, video_url, tagged_users, caption_mentions, coauthors, sponsor_tags, and is_paid_partnership. view_count is always null here; use get_user_reels for video play counts.

- Site: instagram.com
- Address: `reduck/instagram.com/get_user_posts`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_user_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_user_posts
```

## Input

- `username` (string, required): Instagram handle without @, e.g. berniesanders
- `count` (integer, optional): Number of most-recent posts to return

## FAQ

### What does "Get Instagram user posts" do?

Fetch the most recent posts from an Instagram user's profile, newest first. Returns code, url, taken_at, media_type, caption, like_count, comment_count, images, video_url, tagged_users, caption_mentions, coauthors, sponsor_tags, and is_paid_partnership. view_count is always null here; use get_user_reels for video play counts.

### How do I automatically get Instagram user posts on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_user_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_user_posts

### Is there a instagram.com API to get Instagram user posts?

You do not need one. "Get Instagram user posts" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: count.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_user_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_user_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_user_posts
