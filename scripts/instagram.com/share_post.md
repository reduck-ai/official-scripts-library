# Share Instagram post via DM

Automatically share Instagram post via DM on instagram.com. Share an Instagram post or reel to a user via DM. Works for both posts and reels; fails loudly if the recipient handle isn't found in search. Returns shortcode, username, and thread_key.

- Site: instagram.com
- Address: `reduck/instagram.com/share_post`
- Updated: 2026-08-27 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/share_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/share_post
```

## Input

- `username` (string, required): Recipient handle without @, e.g. davidguetta
- `shortcode` (string, required): Post or reel shortcode, e.g. the X in instagram.com/p/X/ or /reel/X/

## Output

- `username` (string, required)
- `shortcode` (string, required)
- `thread_key` (string, required): ID of the DM thread the post/reel was delivered into.

## FAQ

### What does "Share Instagram post via DM" do?

Share an Instagram post or reel to a user via DM. Works for both posts and reels; fails loudly if the recipient handle isn't found in search. Returns shortcode, username, and thread_key.

### How do I automatically share Instagram post via DM on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/share_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/share_post

### Is there a instagram.com API to share Instagram post via DM?

You do not need one. "Share Instagram post via DM" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: shortcode, username.

### What does it return?

It returns username, shortcode, thread_key.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/share_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/share_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/share_post
