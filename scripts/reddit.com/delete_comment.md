# Delete Reddit comment

Automatically delete Reddit comment on reddit.com. Delete your own Reddit comment (at any depth) by its permalink. Returns deleted and commentId. This is irreversible, only works on your own comments, and replies to it remain visible under [deleted]. Runs only via the browser extension, not the hosted cloud browser.

- Site: reddit.com
- Address: `reduck/reddit.com/delete_comment`
- Updated: 2026-08-20 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/delete_comment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/delete_comment
```

## Input

- `permalink` (string, required): Comment permalink (full or path), e.g. /r/sub/comments/<postid>/comment/<commentid>/

## Output

- `deleted` (boolean, required)
- `commentId` (string, required)
- `account_used` (string, required): The real logged-in Reddit handle that performed the action, read from the page's own account drawer (not assumed from args)
- `already_present` (boolean, required): True when the comment was already gone (deleted/removed) before this call — idempotent no-op, no mutation attempted
- `verified_on_page` (boolean, required): Whether the script reloaded the comment's permalink afterward and confirmed it's actually gone

## FAQ

### What does "Delete Reddit comment" do?

Delete your own Reddit comment (at any depth) by its permalink. Returns deleted and commentId. This is irreversible, only works on your own comments, and replies to it remain visible under [deleted]. Runs only via the browser extension, not the hosted cloud browser.

### How do I automatically delete Reddit comment on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/delete_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/delete_comment

### Is there a reddit.com API to delete Reddit comment?

You do not need one. "Delete Reddit comment" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: permalink.

### What does it return?

It returns deleted, commentId, account_used, already_present, verified_on_page.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It makes changes on reddit.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/delete_comment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/delete_comment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/delete_comment
