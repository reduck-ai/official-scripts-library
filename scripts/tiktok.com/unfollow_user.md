# Unfollow a TikTok user

Automatically unfollow a TikTok user on tiktok.com. Unfollow a TikTok user (as the logged-in account) by @username. Safe to repeat: it does nothing if you don't follow them.

- Site: tiktok.com
- Address: `reduck/tiktok.com/unfollow_user`
- Updated: 2026-08-26 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/unfollow_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/unfollow_user
```

## Input

- `username` (string, required): TikTok handle, with or without leading @.

## Output

- `changed` (boolean, required): True if this call removed the follow; false if not following to begin with.
- `username` (string, required)
- `following` (boolean, required)

## FAQ

### What does "Unfollow a TikTok user" do?

Unfollow a TikTok user (as the logged-in account) by @username. Safe to repeat: it does nothing if you don't follow them.

### How do I automatically unfollow a TikTok user on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/unfollow_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/unfollow_user

### Is there a tiktok.com API to unfollow a TikTok user?

You do not need one. "Unfollow a TikTok user" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns changed, username, following.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/unfollow_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/unfollow_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/unfollow_user
