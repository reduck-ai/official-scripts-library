# Unsave Instagram post

Automatically unsave Instagram post on instagram.com. Remove an Instagram post or reel from your saved items by shortcode. Clicks the filled action-bar bookmark and confirms the Remove→Save flip. Fails loudly if it wasn't saved (no Remove button) or unavailable. Returns shortcode and saved.

- Site: instagram.com
- Address: `reduck/instagram.com/unsave_post`
- Updated: 2026-09-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/unsave_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/unsave_post
```

## Input

- `shortcode` (string, required): Shortcode of the post/reel (the code in instagram.com/p/<code>/ or /reel/<code>/).

## Output

- `saved` (boolean, required)
- `shortcode` (string, required)
- `alreadyUnsaved` (boolean, optional): True when the post was not saved and nothing was clicked.

## FAQ

### What does "Unsave Instagram post" do?

Remove an Instagram post or reel from your saved items by shortcode. Clicks the filled action-bar bookmark and confirms the Remove→Save flip. Fails loudly if it wasn't saved (no Remove button) or unavailable. Returns shortcode and saved.

### How do I automatically unsave Instagram post on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/unsave_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/unsave_post

### Is there a instagram.com API to unsave Instagram post?

You do not need one. "Unsave Instagram post" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: shortcode.

### What does it return?

It returns saved, shortcode, alreadyUnsaved.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/unsave_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/unsave_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/unsave_post
