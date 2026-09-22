# Delete Instagram post

Automatically delete Instagram post on instagram.com. Delete one of your own Instagram posts or reels by shortcode. Opens the post, drives More options then Delete and the confirmation, and then reloads the post's link to prove it is really gone before reporting success. Returns the shortcode, the media id when Instagram exposes it, and whether the post was verified as removed. Fails clearly when the shortcode is not available to you (already deleted, private, or another account's) and when the post is still live after the confirmation.

- Site: instagram.com
- Address: `reduck/instagram.com/delete_post`
- Updated: 2026-08-28 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/delete_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/delete_post
```

## Input

- `shortcode` (string, required)

## Output

- `shortcode` (string, required)
- `did_delete` (boolean, required)
- `verified_gone` (boolean, required)
- `pk` (string | null, optional)

## FAQ

### What does "Delete Instagram post" do?

Delete one of your own Instagram posts or reels by shortcode. Opens the post, drives More options then Delete and the confirmation, and then reloads the post's link to prove it is really gone before reporting success. Returns the shortcode, the media id when Instagram exposes it, and whether the post was verified as removed. Fails clearly when the shortcode is not available to you (already deleted, private, or another account's) and when the post is still live after the confirmation.

### How do I automatically delete Instagram post on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/delete_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/delete_post

### Is there a instagram.com API to delete Instagram post?

You do not need one. "Delete Instagram post" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: shortcode.

### What does it return?

It returns pk, shortcode, did_delete, verified_gone.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/delete_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/delete_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/delete_post
