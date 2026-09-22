# Delete Instagram comment

Automatically delete Instagram comment on instagram.com. Delete one of your own comments on an Instagram post or reel by its shortcode and comment id. Opens the comment's own permalink, drives its options menu then Delete, and reloads that permalink to prove it is really gone before reporting success. Fails clearly when the comment isn't available (already deleted, wrong id/shortcode) and when its options menu has no Delete entry (a comment that isn't yours).

- Site: instagram.com
- Address: `reduck/instagram.com/delete_comment`
- Updated: 2026-09-01 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/delete_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/delete_comment
```

## Input

- `shortcode` (string, required): Post/reel shortcode (instagram.com/p/<code>/).
- `comment_id` (string, required): Id of the comment to delete, from get_post_comments' id field. Must be a comment you own.

## Output

- `shortcode` (string, required)
- `comment_id` (string, required)
- `did_delete` (boolean, required)
- `verified_gone` (boolean, required): True when the comment's own permalink was reloaded after the delete and no longer resolves to it.

## FAQ

### What does "Delete Instagram comment" do?

Delete one of your own comments on an Instagram post or reel by its shortcode and comment id. Opens the comment's own permalink, drives its options menu then Delete, and reloads that permalink to prove it is really gone before reporting success. Fails clearly when the comment isn't available (already deleted, wrong id/shortcode) and when its options menu has no Delete entry (a comment that isn't yours).

### How do I automatically delete Instagram comment on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/delete_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/delete_comment

### Is there a instagram.com API to delete Instagram comment?

You do not need one. "Delete Instagram comment" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: shortcode, comment_id.

### What does it return?

It returns shortcode, comment_id, did_delete, verified_gone.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/delete_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/delete_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/delete_comment
