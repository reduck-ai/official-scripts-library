# Unfollow Instagram user

Automatically unfollow Instagram user on instagram.com. Unfollow an Instagram user from their profile. Fails loudly if you weren't already following them — including when there's only a pending (not-yet-accepted) follow request to a private account, which this script doesn't withdraw. Returns username, user_id, following, followed_by, and outgoing_request.

- Site: instagram.com
- Address: `reduck/instagram.com/unfollow_user`
- Updated: 2026-09-08 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/unfollow_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/unfollow_user
```

## Input

- `username` (string, required): Instagram handle without @, e.g. calvinharris

## Output

- `user_id` (string, required)
- `username` (string, required)
- `following` (boolean, required): False once unfollow succeeds.
- `followed_by` (boolean, required)
- `outgoing_request` (boolean, required)

## FAQ

### What does "Unfollow Instagram user" do?

Unfollow an Instagram user from their profile. Fails loudly if you weren't already following them — including when there's only a pending (not-yet-accepted) follow request to a private account, which this script doesn't withdraw. Returns username, user_id, following, followed_by, and outgoing_request.

### How do I automatically unfollow Instagram user on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/unfollow_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/unfollow_user

### Is there a instagram.com API to unfollow Instagram user?

You do not need one. "Unfollow Instagram user" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns user_id, username, following, followed_by, outgoing_request.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/unfollow_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/unfollow_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/unfollow_user
