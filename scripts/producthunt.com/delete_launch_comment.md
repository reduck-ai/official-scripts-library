# Delete your comment on a Product Hunt launch

Automatically delete your comment on a Product Hunt launch on producthunt.com. Delete one of the signed-in account's own comments on a Product Hunt launch, by its id. Accepts a full launch URL or a "product/launch" slug pair. If the comment is no longer shown, nothing changes and already_absent is true. A comment written by another account is refused. A signed-out browser fails with a signed-out error. Inverse of post_launch_comment.

- Site: producthunt.com
- Address: `reduck/producthunt.com/delete_launch_comment`
- Updated: 2026-11-02 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/producthunt.com/delete_launch_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/producthunt.com/delete_launch_comment
```

## Input

- `launch` (string, required): Full launch URL or a "product/launch" slug pair, the launch the comment is on.
- `comment_id` (string, required): Id of your comment, as returned by post_launch_comment or get_launch_comments.

## Output

- `deleted` (boolean, required): True when this run deleted the comment.
- `launchUrl` (string, required)
- `comment_id` (string, required)
- `account_used` (string, required): Handle of the signed-in account, read from the session.
- `already_absent` (boolean, required): True when the comment was not shown on the launch, so nothing was done.
- `verified_on_page` (boolean, required): True when Product Hunt confirmed the deletion and the comment left the thread.

## FAQ

### What does "Delete your comment on a Product Hunt launch" do?

Delete one of the signed-in account's own comments on a Product Hunt launch, by its id. Accepts a full launch URL or a "product/launch" slug pair. If the comment is no longer shown, nothing changes and already_absent is true. A comment written by another account is refused. A signed-out browser fails with a signed-out error. Inverse of post_launch_comment.

### How do I automatically delete your comment on a Product Hunt launch on producthunt.com?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/delete_launch_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/delete_launch_comment

### Is there a producthunt.com API to delete your comment on a Product Hunt launch?

You do not need one. "Delete your comment on a Product Hunt launch" drives the real producthunt.com pages in a browser, so it works whether or not producthunt.com offers an API for this.

### What information do I need to provide?

Required: launch, comment_id.

### What does it return?

It returns deleted, launchUrl, comment_id, account_used, already_absent, verified_on_page.

### Do I need to be logged in to producthunt.com?

Yes. It acts as you on producthunt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the producthunt.com cookies saved by the Reduck extension.

### Does it change anything on producthunt.com, or only read data?

It makes changes on producthunt.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/delete_launch_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/delete_launch_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/producthunt.com/delete_launch_comment
