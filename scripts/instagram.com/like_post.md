# Like Instagram post

Automatically like Instagram post on instagram.com. Like an Instagram post or reel by shortcode. Clicks the action-bar heart and confirms the Like→Unlike flip (server-driven). Fails loudly if the post is already liked (no Like button) or unavailable. Returns shortcode and liked.

- Site: instagram.com
- Address: `reduck/instagram.com/like_post`
- Updated: 2026-08-27 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/like_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/like_post
```

## Input

- `shortcode` (string, required): Shortcode of the post/reel (the code in instagram.com/p/<code>/ or /reel/<code>/).

## Output

- `liked` (boolean, required)
- `shortcode` (string, required)
- `alreadyLiked` (boolean, optional): True when the post was already liked and nothing was clicked.

## FAQ

### What does "Like Instagram post" do?

Like an Instagram post or reel by shortcode. Clicks the action-bar heart and confirms the Like→Unlike flip (server-driven). Fails loudly if the post is already liked (no Like button) or unavailable. Returns shortcode and liked.

### How do I automatically like Instagram post on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/like_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/like_post

### Is there a instagram.com API to like Instagram post?

You do not need one. "Like Instagram post" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: shortcode.

### What does it return?

It returns liked, shortcode, alreadyLiked.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/like_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/like_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/like_post
