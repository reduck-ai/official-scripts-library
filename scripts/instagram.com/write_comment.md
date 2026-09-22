# Post Instagram comment

Automatically post Instagram comment on instagram.com. Post a comment on an Instagram post or reel by its shortcode. Returns comment_id, shortcode, comment, username, and created_at.

- Site: instagram.com
- Address: `reduck/instagram.com/write_comment`
- Updated: 2026-08-27 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/write_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/write_comment
```

## Input

- `comment` (string, required): Comment text to post.
- `shortcode` (string, required): Post/reel shortcode, e.g. 'DZe2-RZKgQG' from instagram.com/p/<shortcode>/ (reels work via /p/ too).

## Output

- `comment` (string, required)
- `username` (string, required): Commenter (the logged-in account).
- `shortcode` (string, required)
- `comment_id` (string, required): Server-assigned comment pk.
- `created_at` (number, required): Unix epoch seconds.

## FAQ

### What does "Post Instagram comment" do?

Post a comment on an Instagram post or reel by its shortcode. Returns comment_id, shortcode, comment, username, and created_at.

### How do I automatically post Instagram comment on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/write_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/write_comment

### Is there a instagram.com API to post Instagram comment?

You do not need one. "Post Instagram comment" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: shortcode, comment.

### What does it return?

It returns comment, username, shortcode, comment_id, created_at.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/write_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/write_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/write_comment
