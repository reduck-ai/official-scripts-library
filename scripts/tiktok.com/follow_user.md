# Follow a TikTok user

Automatically follow a TikTok user on tiktok.com. Follow a TikTok user (as the logged-in account) by @username. Safe to repeat: it does nothing if you already follow them.

- Site: tiktok.com
- Address: `reduck/tiktok.com/follow_user`
- Updated: 2026-09-16 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/follow_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/follow_user
```

## Input

- `username` (string, required): TikTok handle, with or without leading @. The account must exist and be viewable by the signed-in account: a handle that does not exist, or one TikTok will not show (private, restricted, or gated by the creator's audience controls), is refused rather than followed, because TikTok renders no follow button on those profiles.

## Output

- `changed` (boolean, required): True if this call started the follow; false if already following.
- `username` (string, required)
- `following` (boolean, required)

## FAQ

### What does "Follow a TikTok user" do?

Follow a TikTok user (as the logged-in account) by @username. Safe to repeat: it does nothing if you already follow them.

### How do I automatically follow a TikTok user on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/follow_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/follow_user

### Is there a tiktok.com API to follow a TikTok user?

You do not need one. "Follow a TikTok user" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns changed, username, following.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/follow_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/follow_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/follow_user
