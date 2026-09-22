# Unfollow Reddit user

Automatically unfollow Reddit user on reddit.com. Unfollow a Reddit user by username. If you're not following them, nothing changes and changed is returned as false. Runs only via the browser extension, not the hosted cloud browser.

- Site: reddit.com
- Address: `reduck/reddit.com/unfollow_user`
- Updated: 2026-07-31 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/unfollow_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/unfollow_user
```

## Input

- `username` (string, required): Reddit username, with or without u/ prefix

## Output

- `changed` (boolean, required): False when not following (no click, no mutation)
- `username` (string, required)
- `following` (boolean, required)

## FAQ

### What does "Unfollow Reddit user" do?

Unfollow a Reddit user by username. If you're not following them, nothing changes and changed is returned as false. Runs only via the browser extension, not the hosted cloud browser.

### How do I automatically unfollow Reddit user on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/unfollow_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/unfollow_user

### Is there a reddit.com API to unfollow Reddit user?

You do not need one. "Unfollow Reddit user" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns changed, username, following.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It makes changes on reddit.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/unfollow_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/unfollow_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/unfollow_user
