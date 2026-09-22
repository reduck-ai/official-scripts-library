# Edit Reddit post

Automatically edit Reddit post on reddit.com. Edit the body of your own Reddit text post by its URL, replacing it entirely. Returns edited and postId. Text posts only (the title can't be edited on Reddit); only works on your own posts. Runs only via the browser extension, not the hosted cloud browser.

- Site: reddit.com
- Address: `reduck/reddit.com/edit_post`
- Updated: 2026-09-14 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/edit_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/edit_post
```

## Input

- `url` (string, required): Post URL (full or path)
- `body` (string, required): New body text (replaces the existing body entirely)

## Output

- `body` (string, required)
- `edited` (boolean, required): False when the post's body already matched exactly (idempotent no-op, no mutation)
- `postId` (string, required)
- `account_used` (string, required): The real logged-in Reddit handle that performed the action, read from the page's own account drawer (not assumed from args)
- `already_present` (boolean, required): True when the post's body was already exactly the requested text before this call
- `verified_on_page` (boolean, required): Whether the script reloaded the post afterward and confirmed the new body is actually visible there

## FAQ

### What does "Edit Reddit post" do?

Edit the body of your own Reddit text post by its URL, replacing it entirely. Returns edited and postId. Text posts only (the title can't be edited on Reddit); only works on your own posts. Runs only via the browser extension, not the hosted cloud browser.

### How do I automatically edit Reddit post on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/edit_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/edit_post

### Is there a reddit.com API to edit Reddit post?

You do not need one. "Edit Reddit post" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: url, body.

### What does it return?

It returns body, edited, postId, account_used, already_present, verified_on_page.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It makes changes on reddit.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/edit_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/edit_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/edit_post
