# Follow X user

Automatically follow X user on x.com. Follow an X user. Returns handle, was_following, is_following, status. Already-following accounts are reported rather than re-followed; errors on missing or suspended accounts.

- Site: x.com
- Address: `reduck/x.com/follow_user`
- Updated: 2026-09-03 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/follow_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/follow_user
```

## Input

- `handle` (string, required): X handle without the leading @ (e.g. 'jaminball'). The follow takes effect immediately (or a follow request is sent, for protected accounts) and is visible to the target account and to anyone viewing your following list, so confirm the exact handle with the user before running rather than inferring it from an earlier or unrelated message.

## Output

- `handle` (string, required)
- `is_following` (boolean, required): Follow-state read back after the action - true only once actually following; stays false for a pending request to a protected account, since X doesn't count that as following until they approve.
- `was_following` (boolean, required): already_present signal: true if already following, or a request was already pending, on arrival.
- `verified_on_page` (boolean, required): true if the page was reloaded and re-inspected after the action, confirming the resulting state is actually visible/present
- `status` (any, optional): followed = the button flipped to Following/Unfollow after our click; already_following = it was already in that state; requested = the target account is protected/locked, so a follow request was sent (or one was already pending) instead of following immediately - is_following stays false until they approve it.
- `account_used` (string | null, optional): handle of the logged-in account that performed the action, read from the account switcher UI (not assumed from input)

## FAQ

### What does "Follow X user" do?

Follow an X user. Returns handle, was_following, is_following, status. Already-following accounts are reported rather than re-followed; errors on missing or suspended accounts.

### How do I automatically follow X user on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/follow_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/follow_user

### Is there a x.com API to follow X user?

You do not need one. "Follow X user" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: handle.

### What does it return?

It returns handle, status, account_used, is_following, was_following, verified_on_page.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/follow_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/follow_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/follow_user
