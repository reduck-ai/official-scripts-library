# Delete your own comment on a Facebook post

Automatically delete your own comment on a Facebook post on facebook.com. Delete a comment you left on a Facebook post. Pass the post's URL and the exact text of the comment. Only your own comments can be deleted: on someone else's comment Facebook offers no delete option and the script says so instead of clicking anything. Returns deleted once the comment is gone from the page, or already_gone when no comment with that text was there to begin with. Works in any interface language.

- Site: facebook.com
- Address: `reduck/facebook.com/delete_own_comment`
- Updated: 2026-11-13 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/delete_own_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/delete_own_comment
```

## Input

- `text` (string, required): Exact text of the comment to delete
- `postUrl` (string, required): Full URL of the Facebook post the comment sits on. To delete a reply, pass the reply's own link (as returned by reply_to_comment): replies are collapsed on the plain post link and would be reported as already gone.

## Output

- `status` (string, required)
- `text` (string, optional)
- `accountId` (string, optional)

## FAQ

### What does "Delete your own comment on a Facebook post" do?

Delete a comment you left on a Facebook post. Pass the post's URL and the exact text of the comment. Only your own comments can be deleted: on someone else's comment Facebook offers no delete option and the script says so instead of clicking anything. Returns deleted once the comment is gone from the page, or already_gone when no comment with that text was there to begin with. Works in any interface language.

### How do I automatically delete your own comment on a Facebook post on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/delete_own_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/delete_own_comment

### Is there a facebook.com API to delete your own comment on a Facebook post?

You do not need one. "Delete your own comment on a Facebook post" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: postUrl, text.

### What does it return?

It returns text, status, accountId.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It makes changes on facebook.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/delete_own_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/delete_own_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/delete_own_comment
