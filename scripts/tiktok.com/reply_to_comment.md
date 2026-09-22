# Reply to a TikTok comment

Automatically reply to a TikTok comment on tiktok.com. Publish a reply to a specific comment on a TikTok video, given the video, the comment's id and the text to post. Use this instead of the post-comment script when the reply must sit under an existing comment rather than at the top level. Before posting it checks whether you already left the same reply under that comment, so re-running does not create duplicates, and afterwards it re-reads the comment's replies to confirm the reply is really there and reports which account it was published from. Posting is public and immediate — show the exact text to the person asking and get their confirmation before running this. Use the delete-comment script to remove it again.

- Site: tiktok.com
- Address: `reduck/tiktok.com/reply_to_comment`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/reply_to_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/reply_to_comment
```

## Input

- `text` (string, required): Reply text to publish. Shown publicly under your account.
- `video` (string, required): Full TikTok video URL or a bare numeric video id (the video the comment belongs to).
- `commentId` (string, required): Id of the comment to reply to, as returned by the list-comments script.
- `rootCommentId` (string, optional): Only needed when replying to a reply rather than to a top-level comment: the id of the top-level comment that starts the thread. TikTok threads every reply under that top comment.

## Output

- `posted` (boolean, required): True when this run published a new reply. False when an identical one was already there.
- `videoId` (string, required)
- `already_present` (boolean, required): True when the same account had already posted this exact reply under this comment, so nothing new was published.
- `parentCommentId` (string, required): The comment the reply was threaded under.
- `verified_on_page` (boolean | null, required): True when the reply was found by re-reading the comment's replies, which is retried for a few seconds because that list is eventually consistent. False only when every reply was read without finding it. Null when the reply list was too long to read to the end, so its presence could not be established either way.
- `text` (string | null, optional)
- `commentId` (string | null, optional): Id of the new reply, usable with the delete-comment script.
- `createTime` (integer | null, optional)
- `account_used` (string | null, optional): Handle the reply was actually published from, read from the signed-in session rather than assumed.
- `replyToReplyId` (string | null, optional): Set when the reply targets another reply rather than the top-level comment.
- `parentReplyCount` (integer | null, optional): Replies TikTok reports under the parent comment after posting.

## FAQ

### What does "Reply to a TikTok comment" do?

Publish a reply to a specific comment on a TikTok video, given the video, the comment's id and the text to post. Use this instead of the post-comment script when the reply must sit under an existing comment rather than at the top level. Before posting it checks whether you already left the same reply under that comment, so re-running does not create duplicates, and afterwards it re-reads the comment's replies to confirm the reply is really there and reports which account it was published from. Posting is public and immediate — show the exact text to the person asking and get their confirmation before running this. Use the delete-comment script to remove it again.

### How do I automatically reply to a TikTok comment on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/reply_to_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/reply_to_comment

### Is there a tiktok.com API to reply to a TikTok comment?

You do not need one. "Reply to a TikTok comment" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: video, commentId, text. Optional: rootCommentId.

### What does it return?

It returns text, posted, videoId, commentId, createTime, account_used, replyToReplyId, already_present, parentCommentId, parentReplyCount, verified_on_page.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/reply_to_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/reply_to_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/reply_to_comment
