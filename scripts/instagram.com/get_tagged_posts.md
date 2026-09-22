# Get Instagram tagged posts

Automatically get Instagram tagged posts on instagram.com. Fetch posts an Instagram user is tagged in, by their numeric user_id (from get_profile). Returns total_count, next_max_id (pass back as max_id to paginate), and posts (code, url, owner, like_count, comment_count, caption, thumbnail, media_type, taken_at). Only tagged posts the account allows to be shown are returned.

- Site: instagram.com
- Address: `reduck/instagram.com/get_tagged_posts`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_tagged_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_tagged_posts
```

## Input

- `user_id` (string, required): Numeric user id of the tagged account (get_profile returns it as user_id).
- `count` (integer, optional): Max posts per page.
- `max_id` (string, optional): Pagination cursor from a previous call's next_max_id. Omit for the first page.

## Output

- `posts` (array, required)
- `user_id` (string, required)
- `next_max_id` (string | null, optional)
- `total_count` (integer | null, optional)

## FAQ

### What does "Get Instagram tagged posts" do?

Fetch posts an Instagram user is tagged in, by their numeric user_id (from get_profile). Returns total_count, next_max_id (pass back as max_id to paginate), and posts (code, url, owner, like_count, comment_count, caption, thumbnail, media_type, taken_at). Only tagged posts the account allows to be shown are returned.

### How do I automatically get Instagram tagged posts on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_tagged_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_tagged_posts

### Is there a instagram.com API to get Instagram tagged posts?

You do not need one. "Get Instagram tagged posts" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: user_id. Optional: count, max_id.

### What does it return?

It returns posts, user_id, next_max_id, total_count.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

Unknown: its author has not declared whether it changes anything on instagram.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_tagged_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_tagged_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_tagged_posts
