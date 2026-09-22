# Get Instagram comment replies

Automatically get Instagram comment replies on instagram.com. Fetch the threaded replies of a specific comment on a post/reel. Needs the post shortcode and the comment id (from get_post_comments' id field). Returns the parent comment id, child_comment_count, and replies (id, text, user, verified, like_count, created_at). Only returns one page of replies — Instagram doesn't expose further pagination through this method.

- Site: instagram.com
- Address: `reduck/instagram.com/get_comment_replies`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_comment_replies`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_comment_replies
```

## Input

- `shortcode` (string, required): Post/reel shortcode (instagram.com/p/<code>/).
- `comment_id` (string, required): Parent comment id, from get_post_comments' id field.

## Output

- `replies` (array, required)
- `comment_id` (string, required)
- `child_comment_count` (integer | null, optional)

## FAQ

### What does "Get Instagram comment replies" do?

Fetch the threaded replies of a specific comment on a post/reel. Needs the post shortcode and the comment id (from get_post_comments' id field). Returns the parent comment id, child_comment_count, and replies (id, text, user, verified, like_count, created_at). Only returns one page of replies — Instagram doesn't expose further pagination through this method.

### How do I automatically get Instagram comment replies on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_comment_replies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_comment_replies

### Is there a instagram.com API to get Instagram comment replies?

You do not need one. "Get Instagram comment replies" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: shortcode, comment_id.

### What does it return?

It returns replies, comment_id, child_comment_count.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_comment_replies, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_comment_replies

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_comment_replies
