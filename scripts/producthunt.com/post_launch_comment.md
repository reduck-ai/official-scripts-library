# Post a comment on a Product Hunt launch

Automatically post a comment on a Product Hunt launch on producthunt.com. Post a comment on a Product Hunt launch as the signed-in account, or reply to an existing comment by passing its id. Accepts a full launch URL or a "product/launch" slug pair. Returns the new comment in the same shape as get_launch_comments (id, author, text as posted, depth) plus its link and the account used. If this account already left the same text in the same place, nothing is posted and that comment comes back with already_present true. Product Hunt offers to follow the launch's makers when you comment; that is off unless follow_makers is true. A signed-out browser fails with a signed-out error. Undo with delete_launch_comment.

- Site: producthunt.com
- Address: `reduck/producthunt.com/post_launch_comment`
- Updated: 2026-11-23 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/producthunt.com/post_launch_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/producthunt.com/post_launch_comment
```

## Input

- `text` (string, required): The comment text to post. For a reply it replaces the mentions Product Hunt pre-fills.
- `launch` (string, required): Full launch URL (e.g. "https://www.producthunt.com/products/notion/launches/notion-mail") or a "product/launch" slug pair (e.g. "notion/notion-mail").
- `follow_makers` (boolean, optional): Product Hunt offers to follow the launch's hunter and product when you comment. False (default) leaves them unfollowed; true follows them.
- `reply_to_comment_id` (string, optional): Optional id of a comment on this launch to reply to, as returned by get_launch_comments. Omit for a top-level comment.

## Output

- `id` (string, required): Product Hunt's id for the comment.
- `url` (string, required): Link to the comment on the launch page.
- `body` (string, required): The comment text as Product Hunt shows it.
- `depth` (number, required): 0 for a top-level comment, 1 for a reply, and so on.
- `launchUrl` (string, required)
- `account_used` (string, required): Handle of the signed-in account, read from the session.
- `authorHandle` (string, required)
- `already_present` (boolean, required): True when this account had already posted the same text in the same place, so nothing was posted.
- `verified_on_page` (boolean, required): True when Product Hunt confirmed the comment and the thread shows it.
- `pinned` (boolean, optional)
- `upvotes` (number | null, optional)
- `postedAt` (string | null, optional)
- `authorName` (string | null, optional)
- `authorUserId` (string | null, optional)
- `authorSubtitle` (string | null, optional)
- `reply_to_comment_id` (string | null, optional)

## FAQ

### What does "Post a comment on a Product Hunt launch" do?

Post a comment on a Product Hunt launch as the signed-in account, or reply to an existing comment by passing its id. Accepts a full launch URL or a "product/launch" slug pair. Returns the new comment in the same shape as get_launch_comments (id, author, text as posted, depth) plus its link and the account used. If this account already left the same text in the same place, nothing is posted and that comment comes back with already_present true. Product Hunt offers to follow the launch's makers when you comment; that is off unless follow_makers is true. A signed-out browser fails with a signed-out error. Undo with delete_launch_comment.

### How do I automatically post a comment on a Product Hunt launch on producthunt.com?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/post_launch_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/post_launch_comment

### Is there a producthunt.com API to post a comment on a Product Hunt launch?

You do not need one. "Post a comment on a Product Hunt launch" drives the real producthunt.com pages in a browser, so it works whether or not producthunt.com offers an API for this.

### What information do I need to provide?

Required: launch, text. Optional: follow_makers, reply_to_comment_id.

### What does it return?

It returns id, url, body, depth, pinned, upvotes, postedAt, launchUrl, authorName, account_used, authorHandle, authorUserId, authorSubtitle, already_present, verified_on_page, reply_to_comment_id.

### Do I need to be logged in to producthunt.com?

Yes. It acts as you on producthunt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the producthunt.com cookies saved by the Reduck extension.

### Does it change anything on producthunt.com, or only read data?

It makes changes on producthunt.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/post_launch_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/post_launch_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/producthunt.com/post_launch_comment
