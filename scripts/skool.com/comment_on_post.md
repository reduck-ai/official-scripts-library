# Comment on a Skool post

Automatically comment on a Skool post on skool.com. Add a comment to a Skool community post, addressed by the post's URL. Returns the account that commented, a preview of what was published, and whether an identical comment from that account was already on the post before this ran, so a repeated call is visible rather than silently duplicated. The comment is confirmed by reading it back from the post itself after publishing, not from the editor. This is a write: the comment is visible to everyone who can see the post.

- Site: skool.com
- Address: `reduck/skool.com/comment_on_post`
- Updated: 2026-09-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/skool.com/comment_on_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/skool.com/comment_on_post
```

## Input

- `comment` (string, required): Text of the comment to publish. Line breaks are preserved.
- `postUrl` (string, required): Full URL of the Skool post, e.g. https://www.skool.com/<community>/<post-slug>

## Output

- `posted` (boolean, required): True only when the comment was found on the post after publishing.
- `postUrl` (string, required)
- `accountUsed` (string | null, optional): Handle that published the comment, read from the signed-in session rather than assumed.
- `alreadyPresent` (boolean, optional): True when an identical comment from this account was already on the post before this run, so a repeat call is visible instead of silently duplicating.
- `commentPreview` (string | null, optional): First part of the comment as it appears on the post after publishing.

## FAQ

### What does "Comment on a Skool post" do?

Add a comment to a Skool community post, addressed by the post's URL. Returns the account that commented, a preview of what was published, and whether an identical comment from that account was already on the post before this ran, so a repeated call is visible rather than silently duplicated. The comment is confirmed by reading it back from the post itself after publishing, not from the editor. This is a write: the comment is visible to everyone who can see the post.

### How do I automatically comment on a Skool post on skool.com?

Ask an AI agent connected to Reduck to run reduck/skool.com/comment_on_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/skool.com/comment_on_post

### Is there a skool.com API to comment on a Skool post?

You do not need one. "Comment on a Skool post" drives the real skool.com pages in a browser, so it works whether or not skool.com offers an API for this.

### What information do I need to provide?

Required: postUrl, comment.

### What does it return?

It returns posted, postUrl, accountUsed, alreadyPresent, commentPreview.

### Do I need to be logged in to skool.com?

Yes. It acts as you on skool.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the skool.com cookies saved by the Reduck extension.

### Does it change anything on skool.com, or only read data?

It makes changes on skool.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/skool.com/comment_on_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/skool.com/comment_on_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/skool.com/comment_on_post
