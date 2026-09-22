# Unlike Instagram comment

Automatically unlike Instagram comment on instagram.com. Remove your like from a specific comment on a post/reel. Needs the post shortcode and the comment id (from get_post_comments' id field). Locates the comment via its /c/<id>/ permalink, clicks its filled heart, and confirms the Unlike→Like flip. Fails loudly if it wasn't liked or the comment isn't found. Returns shortcode, comment_id, liked.

- Site: instagram.com
- Address: `reduck/instagram.com/unlike_comment`
- Updated: 2026-08-27 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/unlike_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/unlike_comment
```

## Input

- `shortcode` (string, required): Post/reel shortcode (instagram.com/p/<code>/).
- `comment_id` (string, required): Comment id, from get_post_comments' id field.

## Output

- `liked` (boolean, required)
- `shortcode` (string, required)
- `comment_id` (string, required)
- `alreadyUnliked` (boolean, optional): True when the comment was not liked and nothing was clicked.

## FAQ

### What does "Unlike Instagram comment" do?

Remove your like from a specific comment on a post/reel. Needs the post shortcode and the comment id (from get_post_comments' id field). Locates the comment via its /c/<id>/ permalink, clicks its filled heart, and confirms the Unlike→Like flip. Fails loudly if it wasn't liked or the comment isn't found. Returns shortcode, comment_id, liked.

### How do I automatically unlike Instagram comment on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/unlike_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/unlike_comment

### Is there a instagram.com API to unlike Instagram comment?

You do not need one. "Unlike Instagram comment" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: shortcode, comment_id.

### What does it return?

It returns liked, shortcode, comment_id, alreadyUnliked.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/unlike_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/unlike_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/unlike_comment
