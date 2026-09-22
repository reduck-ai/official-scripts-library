# Save Reddit post

Automatically save Reddit post on reddit.com. Save a Reddit post to your saved list by its URL. If it's already saved, nothing changes and changed is returned as false. Saving is private (visible only in your own saved list). Runs only via the browser extension, not the hosted cloud browser.

- Site: reddit.com
- Address: `reduck/reddit.com/save_post`
- Updated: 2026-09-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/save_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/save_post
```

## Input

- `url` (string, required): Post URL (full or path)

## Output

- `saved` (boolean, required)
- `postId` (string, required)
- `changed` (boolean, required): False when already saved (no click, no mutation)

## FAQ

### What does "Save Reddit post" do?

Save a Reddit post to your saved list by its URL. If it's already saved, nothing changes and changed is returned as false. Saving is private (visible only in your own saved list). Runs only via the browser extension, not the hosted cloud browser.

### How do I automatically save Reddit post on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/save_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/save_post

### Is there a reddit.com API to save Reddit post?

You do not need one. "Save Reddit post" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns saved, postId, changed.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It makes changes on reddit.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/save_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/save_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/save_post
