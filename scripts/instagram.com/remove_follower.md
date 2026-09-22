# Remove a follower

Automatically remove a follower on instagram.com. Remove a follower from the signed-in Instagram account. Irreversible from Instagram's own UI — the removed account would have to refollow to reconnect.

- Site: instagram.com
- Address: `reduck/instagram.com/remove_follower`
- Updated: 2026-09-22 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/remove_follower`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/remove_follower
```

## Input

- `username` (string, required): The follower's username to remove

## Output

- `removed` (boolean, required)
- `username` (string, required)

## FAQ

### What does "Remove a follower" do?

Remove a follower from the signed-in Instagram account. Irreversible from Instagram's own UI — the removed account would have to refollow to reconnect.

### How do I automatically remove a follower on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/remove_follower, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/remove_follower

### Is there a instagram.com API to remove a follower?

You do not need one. "Remove a follower" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns removed, username.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/remove_follower, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/remove_follower

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/remove_follower
