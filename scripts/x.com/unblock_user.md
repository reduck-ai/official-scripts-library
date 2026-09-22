# Unblock X user

Automatically unblock X user on x.com. Unblock an X user by handle. Accounts that aren't blocked are reported rather than erroring. Returns handle, blocked, was_blocked.

- Site: x.com
- Address: `reduck/x.com/unblock_user`
- Updated: 2026-09-03 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/unblock_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/unblock_user
```

## Input

- `handle` (string, required): Target user's handle (with or without @).

## Output

- `handle` (string, required)
- `blocked` (boolean, required)
- `was_blocked` (boolean, required): already_present signal: true if blocked before this call
- `verified_on_page` (boolean, required): true if the page was reloaded and re-inspected after the action, confirming the unblock is actually visible/present
- `account_used` (string | null, optional): handle of the logged-in account that performed the action, read from the account switcher UI (not assumed from input)

## FAQ

### What does "Unblock X user" do?

Unblock an X user by handle. Accounts that aren't blocked are reported rather than erroring. Returns handle, blocked, was_blocked.

### How do I automatically unblock X user on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/unblock_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/unblock_user

### Is there a x.com API to unblock X user?

You do not need one. "Unblock X user" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: handle.

### What does it return?

It returns handle, blocked, was_blocked, account_used, verified_on_page.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/unblock_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/unblock_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/unblock_user
