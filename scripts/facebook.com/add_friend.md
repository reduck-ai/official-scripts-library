# Send Facebook friend request

Automatically send Facebook friend request on facebook.com. Send a friend request to a Facebook profile (pass its URL or numeric userId), only when the profile is addable. Returns status: sent / already_pending / already_friends / not_addable. Does not confirm incoming requests; the request is reversible by canceling it from the profile. Works in either the French or the English interface.

- Site: facebook.com
- Address: `reduck/facebook.com/add_friend`
- Updated: 2026-09-03 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/add_friend`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/add_friend
```

## Input

- `profile` (string, required): Profile URL (https://www.facebook.com/<id-or-username>) or a bare numeric userId / username.

## Output

- `name` (string | null, optional): Profile display name.
- `status` (string, optional)
- `profileUrl` (string, optional)

## FAQ

### What does "Send Facebook friend request" do?

Send a friend request to a Facebook profile (pass its URL or numeric userId), only when the profile is addable. Returns status: sent / already_pending / already_friends / not_addable. Does not confirm incoming requests; the request is reversible by canceling it from the profile. Works in either the French or the English interface.

### How do I automatically send Facebook friend request on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/add_friend, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/add_friend

### Is there a facebook.com API to send Facebook friend request?

You do not need one. "Send Facebook friend request" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: profile.

### What does it return?

It returns name, status, profileUrl.

### Do I need to be logged in to facebook.com?

No. It only uses pages of facebook.com that are reachable without signing in.

### Does it change anything on facebook.com, or only read data?

It makes changes on facebook.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/add_friend, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/add_friend

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/add_friend
