# Follow Instagram user

Automatically follow Instagram user on instagram.com. Follow an Instagram user from their profile. outgoing_request=true means a pending request to a private account; fails if there's no Follow button (already followed/requested). Returns following, outgoing_request, followed_by, user_id.

- Site: instagram.com
- Address: `reduck/instagram.com/follow_user`
- Updated: 2026-08-27 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/follow_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/follow_user
```

## Input

- `username` (string, required): Instagram handle without @, e.g. davidguetta

## Output

- `user_id` (string, required)
- `username` (string, required)
- `following` (boolean, required): True once the follow is active (public accounts). False with outgoing_request=true means a pending request to a private account.
- `followed_by` (boolean, required): Whether the target already follows the caller back.
- `outgoing_request` (boolean, required): True when the target is private and the follow request is awaiting approval.

## FAQ

### What does "Follow Instagram user" do?

Follow an Instagram user from their profile. outgoing_request=true means a pending request to a private account; fails if there's no Follow button (already followed/requested). Returns following, outgoing_request, followed_by, user_id.

### How do I automatically follow Instagram user on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/follow_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/follow_user

### Is there a instagram.com API to follow Instagram user?

You do not need one. "Follow Instagram user" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns user_id, username, following, followed_by, outgoing_request.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/follow_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/follow_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/follow_user
