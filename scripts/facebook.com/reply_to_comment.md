# Reply to a Facebook comment

Automatically reply to a Facebook comment on facebook.com. Reply to a comment on a Facebook post, as the signed-in account. Pass the comment's link (from list_notifications, or the comment's own timestamp link), the commenter's display name and the reply text. Nothing is posted when the comment the link names is by someone else, and when the same reply is already in the thread it is not posted again. Returns the link to the reply, which delete_own_comment takes to remove it. Works in any interface language.

- Site: facebook.com
- Address: `reduck/facebook.com/reply_to_comment`
- Updated: 2026-11-13 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/reply_to_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/reply_to_comment
```

## Input

- `url` (string, required): Link to the comment to reply to, as given by list_notifications or by the comment's own timestamp: the post link carrying the comment's id. A plain post link works only when the commenter has a single comment on the post.
- `author` (string, required): Commenter's display name exactly as shown on the comment. Nothing is posted if the comment the link names is by someone else.
- `message` (string, required): Plain-text reply body.

## Output

- `status` (string, required)
- `replyUrl` (string | null, required): Link to the reply itself: the one just posted, or the identical one that was already there.

## FAQ

### What does "Reply to a Facebook comment" do?

Reply to a comment on a Facebook post, as the signed-in account. Pass the comment's link (from list_notifications, or the comment's own timestamp link), the commenter's display name and the reply text. Nothing is posted when the comment the link names is by someone else, and when the same reply is already in the thread it is not posted again. Returns the link to the reply, which delete_own_comment takes to remove it. Works in any interface language.

### How do I automatically reply to a Facebook comment on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/reply_to_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/reply_to_comment

### Is there a facebook.com API to reply to a Facebook comment?

You do not need one. "Reply to a Facebook comment" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: url, author, message.

### What does it return?

It returns status, replyUrl.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It makes changes on facebook.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/reply_to_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/reply_to_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/reply_to_comment
