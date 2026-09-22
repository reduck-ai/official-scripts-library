# Delete LinkedIn comment

Automatically delete LinkedIn comment on linkedin.com. Permanently delete one of the logged-in member's own comments (or replies) on a LinkedIn post, by the post's permalink plus the comment's urn (from get_post_comments, comment_post, or reply_post_comment). Posts a real, permanent deletion under the logged-in account — this also removes all likes and replies on that comment. If the comment is already gone, it returns already_deleted instead of throwing an error. Refuses to guess on a comment that isn't the account's own (no Delete option in its control menu).

- Site: linkedin.com
- Address: `reduck/linkedin.com/delete_comment`
- Updated: 2026-09-03 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/delete_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/delete_comment
```

## Input

- `postUrl` (string, required): LinkedIn post permalink (/feed/update/urn:li:activity:.../ or /posts/...).
- `commentUrn` (string, required): The comment's urn to delete, e.g. urn:li:comment:(urn:li:activity:123,456) or urn:li:comment:(activity:123,456) (from get_post_comments / comment_post / reply_post_comment). Works for both top-level comments and replies.

## Output

- `deleted` (boolean, required): True once this run's own Delete confirmation went through.
- `postUrl` (string, required)
- `commentUrn` (string, required)
- `already_deleted` (boolean, required): True if the comment could not be found on the post after a full hydrate-and-scroll pass -- treated as already gone, so nothing was clicked.
- `post_had_no_comments` (boolean, optional): Only meaningful when already_deleted is true. True when the post carries no comments at all (scrolled to the bottom of the comment container with zero comment nodes), false when other comments were present but not this one. A post that never hydrates past its skeleton still throws rather than reporting either.

## FAQ

### What does "Delete LinkedIn comment" do?

Permanently delete one of the logged-in member's own comments (or replies) on a LinkedIn post, by the post's permalink plus the comment's urn (from get_post_comments, comment_post, or reply_post_comment). Posts a real, permanent deletion under the logged-in account — this also removes all likes and replies on that comment. If the comment is already gone, it returns already_deleted instead of throwing an error. Refuses to guess on a comment that isn't the account's own (no Delete option in its control menu).

### How do I automatically delete LinkedIn comment on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/delete_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/delete_comment

### Is there a linkedin.com API to delete LinkedIn comment?

You do not need one. "Delete LinkedIn comment" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: postUrl, commentUrn.

### What does it return?

It returns deleted, postUrl, commentUrn, already_deleted, post_had_no_comments.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/delete_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/delete_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/delete_comment
