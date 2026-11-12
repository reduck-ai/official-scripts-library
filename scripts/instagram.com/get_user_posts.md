# Get Instagram user posts

Automatically get Instagram user posts on instagram.com. Fetch the posts of an Instagram user's profile grid, in the order the grid shows them: the posts the owner pinned first, then newest first. Returns posts and complete. Each post has code, url, taken_at, pinned, media_type, caption, like_count (null when the owner hides likes), comment_count, images, video_url, video_duration, carousel_items, tagged_users, caption_mentions, coauthors, sponsor_tags and is_paid_partnership. Reads up to count posts (default 25); complete is true only when the end of the grid was reached, false when count stopped it first. An account with no posts returns an empty list. A username that does not exist, or a private account this account does not follow, fails with an error that says so. view_count is always null here; use get_user_reels for video play counts.

- Site: instagram.com
- Address: `reduck/instagram.com/get_user_posts`
- Updated: 2026-11-11 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_user_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_user_posts
```

## Input

- `username` (string, required): Instagram username without the @, e.g. "nasa"
- `count` (integer, optional): Maximum number of posts to return, in the order the profile grid shows them.

## Output

- `posts` (array, required)
- `complete` (boolean, required): True when the profile has no posts beyond these. False when count stopped the list first.

## FAQ

### What does "Get Instagram user posts" do?

Fetch the posts of an Instagram user's profile grid, in the order the grid shows them: the posts the owner pinned first, then newest first. Returns posts and complete. Each post has code, url, taken_at, pinned, media_type, caption, like_count (null when the owner hides likes), comment_count, images, video_url, video_duration, carousel_items, tagged_users, caption_mentions, coauthors, sponsor_tags and is_paid_partnership. Reads up to count posts (default 25); complete is true only when the end of the grid was reached, false when count stopped it first. An account with no posts returns an empty list. A username that does not exist, or a private account this account does not follow, fails with an error that says so. view_count is always null here; use get_user_reels for video play counts.

### How do I automatically get Instagram user posts on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_user_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_user_posts

### Is there a instagram.com API to get Instagram user posts?

You do not need one. "Get Instagram user posts" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: count.

### What does it return?

It returns posts, complete.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_user_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_user_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_user_posts
