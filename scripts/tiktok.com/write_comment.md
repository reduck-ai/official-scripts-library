# Post a comment on a TikTok video

Automatically post a comment on a TikTok video on tiktok.com. Publish a comment on a TikTok video, given the video's URL or id and the text to post. Before posting it checks whether you have already left the exact same comment on that video, so re-running does not create duplicates. After posting it re-reads the video's comments to confirm the comment is really there, and tells you which account it was published from. Posting is public and immediate — show the exact text to the person asking and get their confirmation before running this. Use the companion delete-comment script to remove it again.

- Site: tiktok.com
- Address: `reduck/tiktok.com/write_comment`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/write_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/write_comment
```

## Input

- `text` (string, required): Comment text to publish. Shown publicly under your account.
- `video` (string, required): Full TikTok video URL or a bare numeric video id.

## Output

- `posted` (boolean, required): True when this run published a new comment. False when an identical comment was already there.
- `videoId` (string, required)
- `already_present` (boolean, required): True when the same account had already posted this exact text on this video, so nothing new was published.
- `verified_on_page` (boolean | null, required): True when the comment was found by re-reading the video's comments. False only when the whole comment list was read without finding it. Null when the list was too long to read to the end, so its presence could not be established either way — expect null on videos with very many comments.
- `text` (string | null, optional)
- `commentId` (string | null, optional): Id of the comment, usable with the delete-comment script.
- `createTime` (integer | null, optional)
- `account_used` (string | null, optional): Handle the comment was actually published from, read from the signed-in session rather than assumed.

## FAQ

### What does "Post a comment on a TikTok video" do?

Publish a comment on a TikTok video, given the video's URL or id and the text to post. Before posting it checks whether you have already left the exact same comment on that video, so re-running does not create duplicates. After posting it re-reads the video's comments to confirm the comment is really there, and tells you which account it was published from. Posting is public and immediate — show the exact text to the person asking and get their confirmation before running this. Use the companion delete-comment script to remove it again.

### How do I automatically post a comment on a TikTok video on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/write_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/write_comment

### Is there a tiktok.com API to post a comment on a TikTok video?

You do not need one. "Post a comment on a TikTok video" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: video, text.

### What does it return?

It returns text, posted, videoId, commentId, createTime, account_used, already_present, verified_on_page.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/write_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/write_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/write_comment
