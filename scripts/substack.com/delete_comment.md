# Delete Substack comment

Automatically delete Substack comment on substack.com. Delete one of the logged-in account's own comments on a Substack post, by the post URL and the comment's id (from post_comment or get_post_comments). Only your own comments can be deleted, and this cannot be undone.

- Site: substack.com
- Address: `reduck/substack.com/delete_comment`
- Updated: 2026-08-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/substack.com/delete_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/substack.com/delete_comment
```

## Input

- `url` (string, required): Full URL of the Substack post the comment is on, e.g. https://example.substack.com/p/my-post-slug. Many publications are served from their own domain rather than *.substack.com; those may be refused, because the signed-in Substack session is not known to reach a publication's own domain.
- `commentId` (number, required): The comment's id, from post_comment's output or get_post_comments

## Output

- `url` (string, required)
- `deleted` (boolean, required): True once Substack's own delete call has answered 200. The script fails rather than returning false, so a returned record always means the comment is gone.
- `commentId` (number, required)

## FAQ

### What does "Delete Substack comment" do?

Delete one of the logged-in account's own comments on a Substack post, by the post URL and the comment's id (from post_comment or get_post_comments). Only your own comments can be deleted, and this cannot be undone.

### How do I automatically delete Substack comment on substack.com?

Ask an AI agent connected to Reduck to run reduck/substack.com/delete_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/substack.com/delete_comment

### Is there a substack.com API to delete Substack comment?

You do not need one. "Delete Substack comment" drives the real substack.com pages in a browser, so it works whether or not substack.com offers an API for this.

### What information do I need to provide?

Required: url, commentId.

### What does it return?

It returns url, deleted, commentId.

### Do I need to be logged in to substack.com?

Yes. It acts as you on substack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the substack.com cookies saved by the Reduck extension.

### Does it change anything on substack.com, or only read data?

It makes changes on substack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/substack.com/delete_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/substack.com/delete_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/substack.com/delete_comment
