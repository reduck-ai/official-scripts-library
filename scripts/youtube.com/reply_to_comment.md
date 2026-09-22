# Reply to YouTube comment

Automatically reply to YouTube comment on youtube.com. Reply to a YouTube comment by id. Returns the new reply's id.

- Site: youtube.com
- Address: `reduck/youtube.com/reply_to_comment`
- Updated: 2026-08-19 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/youtube.com/reply_to_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/youtube.com/reply_to_comment
```

## Input

- `text` (string, required): The reply body to post.
- `video` (string, required): A YouTube video URL (watch?v=, youtu.be/, /shorts/, /embed/) or a bare 11-char video id.
- `commentId` (string, required): The id of the comment to reply to.
- `account` (string, optional): Email (or a distinctive part of it) of the signed-in Google account to reply as, e.g. "tester.account@pointandtest.com". Omit to use the browser's default account. Replying is public and immediate, so when several accounts are signed in, name the intended one rather than relying on the default.

## Output

- `text` (string, required)
- `replyId` (string, required): The id of the newly created reply (format parentId.replyId; use with delete_comment).
- `parentCommentId` (string, required)
- `authuser` (integer | null, optional)
- `repliedAs` (string | null, optional): Email of the account the reply was actually posted as.

## FAQ

### What does "Reply to YouTube comment" do?

Reply to a YouTube comment by id. Returns the new reply's id.

### How do I automatically reply to YouTube comment on youtube.com?

Ask an AI agent connected to Reduck to run reduck/youtube.com/reply_to_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/reply_to_comment

### Is there a youtube.com API to reply to YouTube comment?

You do not need one. "Reply to YouTube comment" drives the real youtube.com pages in a browser, so it works whether or not youtube.com offers an API for this.

### What information do I need to provide?

Required: video, commentId, text. Optional: account.

### What does it return?

It returns text, replyId, authuser, repliedAs, parentCommentId.

### Do I need to be logged in to youtube.com?

Yes. It acts as you on youtube.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the youtube.com cookies saved by the Reduck extension.

### Does it change anything on youtube.com, or only read data?

It makes changes on youtube.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/youtube.com/reply_to_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/reply_to_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/youtube.com/reply_to_comment
