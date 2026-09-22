# Post YouTube comment

Automatically post YouTube comment on youtube.com. Post a top-level comment on a YouTube video. Returns the new commentId.

- Site: youtube.com
- Address: `reduck/youtube.com/post_comment`
- Updated: 2026-08-19 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/youtube.com/post_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/youtube.com/post_comment
```

## Input

- `text` (string, required): The comment body to post.
- `video` (string, required): A YouTube video URL (watch?v=, youtu.be/, /shorts/, /embed/) or a bare 11-char video id.
- `account` (string, optional): Email (or a distinctive part of it) of the signed-in Google account to post as, e.g. "tester.account@pointandtest.com". Omit to use the browser's default account. Posting is public and immediate, so when several accounts are signed in, name the intended one rather than relying on the default.

## Output

- `text` (string, required)
- `videoId` (string, required)
- `postedAs` (string | null, required): Email of the account the comment was actually posted as. Null only when no account was requested and the signed-in email could not be read.
- `commentId` (string, required): The id of the newly created comment (use with delete_comment / reply_to_comment).
- `authuser` (integer | null, optional): The session index the comment was posted under; null when the browser default was used.

## FAQ

### What does "Post YouTube comment" do?

Post a top-level comment on a YouTube video. Returns the new commentId.

### How do I automatically post YouTube comment on youtube.com?

Ask an AI agent connected to Reduck to run reduck/youtube.com/post_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/post_comment

### Is there a youtube.com API to post YouTube comment?

You do not need one. "Post YouTube comment" drives the real youtube.com pages in a browser, so it works whether or not youtube.com offers an API for this.

### What information do I need to provide?

Required: video, text. Optional: account.

### What does it return?

It returns text, videoId, authuser, postedAs, commentId.

### Do I need to be logged in to youtube.com?

Yes. It acts as you on youtube.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the youtube.com cookies saved by the Reduck extension.

### Does it change anything on youtube.com, or only read data?

It makes changes on youtube.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/youtube.com/post_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/post_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/youtube.com/post_comment
