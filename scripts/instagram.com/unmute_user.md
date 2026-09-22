# Unmute a followed account

Automatically unmute a followed account on instagram.com. Unmute a previously muted Instagram account's posts and/or stories (requires following them).

- Site: instagram.com
- Address: `reduck/instagram.com/unmute_user`
- Updated: 2026-09-22 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/unmute_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/unmute_user
```

## Input

- `username` (string, required): The account's username to unmute
- `posts` (boolean, optional): Unmute their posts. Omit to leave unchanged.
- `stories` (boolean, optional): Unmute their stories. Omit to leave unchanged.

## Output

- `username` (string, required)
- `postsMuted` (boolean, required)
- `storiesMuted` (boolean, required)

## FAQ

### What does "Unmute a followed account" do?

Unmute a previously muted Instagram account's posts and/or stories (requires following them).

### How do I automatically unmute a followed account on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/unmute_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/unmute_user

### Is there a instagram.com API to unmute a followed account?

You do not need one. "Unmute a followed account" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: posts, stories.

### What does it return?

It returns username, postsMuted, storiesMuted.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/unmute_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/unmute_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/unmute_user
