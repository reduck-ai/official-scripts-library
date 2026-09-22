# Delete your own Skool comment

Automatically delete your own Skool comment on skool.com. Remove a comment you wrote from a Skool post, identified by the post URL and the text of the comment. Only your own comments can be removed. If the text matches more than one of your comments the run refuses rather than guessing which to remove, and if it matches none it says so without touching the post. Removal is confirmed by reloading the post and checking the comment is gone, not from the confirmation screen. This cannot be undone.

- Site: skool.com
- Address: `reduck/skool.com/delete_comment`
- Updated: 2026-09-18 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/skool.com/delete_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/skool.com/delete_comment
```

## Input

- `postUrl` (string, required): Full URL of the Skool post the comment is on, e.g. https://www.skool.com/<community>/<post-slug>
- `commentText` (string, required): Text from the comment to remove, used to find it. Must match exactly one of your own comments on that post, so give enough of it to be unambiguous.

## Output

- `deleted` (boolean, required): True only when the comment was gone from the post after a reload.
- `postUrl` (string, required)
- `accountUsed` (string | null, optional): Handle whose comment was removed, read from the signed-in session rather than assumed.
- `deletedPreview` (string | null, optional): Start of the comment as it read immediately before removal.

## FAQ

### What does "Delete your own Skool comment" do?

Remove a comment you wrote from a Skool post, identified by the post URL and the text of the comment. Only your own comments can be removed. If the text matches more than one of your comments the run refuses rather than guessing which to remove, and if it matches none it says so without touching the post. Removal is confirmed by reloading the post and checking the comment is gone, not from the confirmation screen. This cannot be undone.

### How do I automatically delete your own Skool comment on skool.com?

Ask an AI agent connected to Reduck to run reduck/skool.com/delete_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/skool.com/delete_comment

### Is there a skool.com API to delete your own Skool comment?

You do not need one. "Delete your own Skool comment" drives the real skool.com pages in a browser, so it works whether or not skool.com offers an API for this.

### What information do I need to provide?

Required: postUrl, commentText.

### What does it return?

It returns deleted, postUrl, accountUsed, deletedPreview.

### Do I need to be logged in to skool.com?

Yes. It acts as you on skool.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the skool.com cookies saved by the Reduck extension.

### Does it change anything on skool.com, or only read data?

It makes changes on skool.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/skool.com/delete_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/skool.com/delete_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/skool.com/delete_comment
