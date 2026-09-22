# Unlike Instagram post

Automatically unlike Instagram post on instagram.com. Remove your like from an Instagram post or reel by shortcode. Clicks the filled action-bar heart and confirms the Unlike→Like flip (server-driven). Fails loudly if the post wasn't liked (no Unlike button) or unavailable. Returns shortcode and liked.

- Site: instagram.com
- Address: `reduck/instagram.com/unlike_post`
- Updated: 2026-08-26 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/unlike_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/unlike_post
```

## Input

- `shortcode` (string, required): Shortcode of the post/reel (the code in instagram.com/p/<code>/ or /reel/<code>/).

## Output

- `liked` (boolean, required)
- `shortcode` (string, required)
- `alreadyUnliked` (boolean, optional): True when the post was not liked and nothing was clicked.

## FAQ

### What does "Unlike Instagram post" do?

Remove your like from an Instagram post or reel by shortcode. Clicks the filled action-bar heart and confirms the Unlike→Like flip (server-driven). Fails loudly if the post wasn't liked (no Unlike button) or unavailable. Returns shortcode and liked.

### How do I automatically unlike Instagram post on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/unlike_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/unlike_post

### Is there a instagram.com API to unlike Instagram post?

You do not need one. "Unlike Instagram post" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: shortcode.

### What does it return?

It returns liked, shortcode, alreadyUnliked.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/unlike_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/unlike_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/unlike_post
