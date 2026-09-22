# Unfollow X user

Automatically unfollow X user on x.com. Unfollow an X user. Returns handle, was_following, is_following, status. Accounts you're not following are reported rather than erroring; errors on missing or suspended accounts.

- Site: x.com
- Address: `reduck/x.com/unfollow_user`
- Updated: 2026-09-03 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/unfollow_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/unfollow_user
```

## Input

- `handle` (string, required): X handle without the leading @ (e.g. 'jaminball'). The unfollow takes effect immediately, so confirm the exact handle with the user before running rather than inferring it from an earlier or unrelated message.

## Output

- `handle` (string, required)
- `is_following` (boolean, required): Follow-state read back after the action — the page's own state indicator, expected false.
- `was_following` (boolean, required): already_present signal: follow state observed on arrival.
- `verified_on_page` (boolean, required): true if the page was reloaded and re-inspected after the action, confirming the unfollow is actually visible/present
- `status` (any, optional): unfollowed = the control flipped back to Follow after we completed whichever confirmation step X required; not_following = there was nothing to unfollow.
- `account_used` (string | null, optional): handle of the logged-in account that performed the action, read from the account switcher UI (not assumed from input)

## FAQ

### What does "Unfollow X user" do?

Unfollow an X user. Returns handle, was_following, is_following, status. Accounts you're not following are reported rather than erroring; errors on missing or suspended accounts.

### How do I automatically unfollow X user on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/unfollow_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/unfollow_user

### Is there a x.com API to unfollow X user?

You do not need one. "Unfollow X user" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: handle.

### What does it return?

It returns handle, status, account_used, is_following, was_following, verified_on_page.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/unfollow_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/unfollow_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/unfollow_user
