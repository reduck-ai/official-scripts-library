# Reply to Instagram comment

Automatically reply to Instagram comment on instagram.com. Post a threaded reply to a specific comment on an Instagram post or reel. Needs the post shortcode, the comment id (from get_post_comments' id field), and the reply text. Returns reply_id, shortcode, comment_id, and the posted text.

- Site: instagram.com
- Address: `reduck/instagram.com/reply_to_comment`
- Updated: 2026-08-28 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/reply_to_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/reply_to_comment
```

## Input

- `text` (string, required): Reply body.
- `shortcode` (string, required): Post/reel shortcode (instagram.com/p/<code>/).
- `comment_id` (string, required): Id of the comment to reply to, from get_post_comments' id field.

## Output

- `reply_id` (string, required)
- `shortcode` (string, required)
- `comment_id` (string, required)
- `text` (string | null, optional)

## FAQ

### What does "Reply to Instagram comment" do?

Post a threaded reply to a specific comment on an Instagram post or reel. Needs the post shortcode, the comment id (from get_post_comments' id field), and the reply text. Returns reply_id, shortcode, comment_id, and the posted text.

### How do I automatically reply to Instagram comment on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/reply_to_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/reply_to_comment

### Is there a instagram.com API to reply to Instagram comment?

You do not need one. "Reply to Instagram comment" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: shortcode, comment_id, text.

### What does it return?

It returns text, reply_id, shortcode, comment_id.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/reply_to_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/reply_to_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/reply_to_comment
