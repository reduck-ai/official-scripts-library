# Unblock Instagram user

Automatically unblock Instagram user on instagram.com. Unblock an Instagram user from their profile. Fails loudly if the profile doesn't render an Unblock button (i.e. they weren't blocked). Returns username, user_id, and blocking.

- Site: instagram.com
- Address: `reduck/instagram.com/unblock_user`
- Updated: 2026-08-28 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/unblock_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/unblock_user
```

## Input

- `username` (string, required): Instagram handle without @, e.g. natgeo

## Output

- `user_id` (string, required)
- `blocking` (boolean, required): False once unblock succeeds.
- `username` (string, required)

## FAQ

### What does "Unblock Instagram user" do?

Unblock an Instagram user from their profile. Fails loudly if the profile doesn't render an Unblock button (i.e. they weren't blocked). Returns username, user_id, and blocking.

### How do I automatically unblock Instagram user on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/unblock_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/unblock_user

### Is there a instagram.com API to unblock Instagram user?

You do not need one. "Unblock Instagram user" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns user_id, blocking, username.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/unblock_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/unblock_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/unblock_user
