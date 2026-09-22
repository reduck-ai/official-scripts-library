# Mute a followed account

Automatically mute a followed account on instagram.com. Mute an Instagram account's posts and/or stories from your feed (requires following them). Instagram does not notify the muted account.

- Site: instagram.com
- Address: `reduck/instagram.com/mute_user`
- Updated: 2026-09-22 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/mute_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/mute_user
```

## Input

- `username` (string, required): The account's username to mute
- `posts` (boolean, optional): Mute their posts from your feed. Omit to leave unchanged.
- `stories` (boolean, optional): Mute their stories. Omit to leave unchanged.

## Output

- `username` (string, required)
- `postsMuted` (boolean, required)
- `storiesMuted` (boolean, required)

## FAQ

### What does "Mute a followed account" do?

Mute an Instagram account's posts and/or stories from your feed (requires following them). Instagram does not notify the muted account.

### How do I automatically mute a followed account on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/mute_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/mute_user

### Is there a instagram.com API to mute a followed account?

You do not need one. "Mute a followed account" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: posts, stories.

### What does it return?

It returns username, postsMuted, storiesMuted.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/mute_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/mute_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/mute_user
