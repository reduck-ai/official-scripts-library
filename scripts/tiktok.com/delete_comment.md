# Delete your own TikTok comment

Automatically delete your own TikTok comment on tiktok.com. Remove a comment you posted on a TikTok video, given the comment's id. Pass the video as well and the script re-reads that video's comments afterwards to confirm the comment is really gone rather than trusting the response. You can only delete comments published from your own account, and deletion cannot be undone.

- Site: tiktok.com
- Address: `reduck/tiktok.com/delete_comment`
- Updated: 2026-08-19 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/delete_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/delete_comment
```

## Input

- `commentId` (string, required): Id of the comment to delete, as returned by the write-comment or get-comments scripts.
- `video` (string, optional): Full TikTok video URL or a bare numeric video id. Optional, but without it the deletion cannot be confirmed by re-reading the comments.

## Output

- `deleted` (boolean, required): True when TikTok accepted the deletion.
- `commentId` (string, required)
- `verified_absent` (boolean | null, required): True when the whole comment list was read and the comment was gone. False when it was still present. Null when no video was supplied, or the list was too long to read to the end — expect null on videos with very many comments.
- `videoId` (string | null, optional)
- `account_used` (string | null, optional): Handle the deletion was performed as, read from the signed-in session rather than assumed.

## FAQ

### What does "Delete your own TikTok comment" do?

Remove a comment you posted on a TikTok video, given the comment's id. Pass the video as well and the script re-reads that video's comments afterwards to confirm the comment is really gone rather than trusting the response. You can only delete comments published from your own account, and deletion cannot be undone.

### How do I automatically delete your own TikTok comment on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/delete_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/delete_comment

### Is there a tiktok.com API to delete your own TikTok comment?

You do not need one. "Delete your own TikTok comment" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: commentId. Optional: video.

### What does it return?

It returns deleted, videoId, commentId, account_used, verified_absent.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/delete_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/delete_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/delete_comment
