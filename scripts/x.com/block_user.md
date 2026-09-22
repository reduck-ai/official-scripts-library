# Block X user

Automatically block X user on x.com. Block an X user by handle. Already-blocked accounts are reported rather than re-blocked. Returns handle, blocked, was_blocked.

- Site: x.com
- Address: `reduck/x.com/block_user`
- Updated: 2026-08-26 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/block_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/block_user
```

## Input

- `handle` (string, required): Target user's handle (with or without @). Blocking takes effect immediately, is visible to the target account, and cuts off your ability to see or interact with them, so confirm the exact handle with the user before running rather than inferring it from an earlier or unrelated message.

## Output

- `handle` (string, required)
- `blocked` (boolean, required)
- `was_blocked` (boolean, required): already_present signal: true if already blocked before this call
- `verified_on_page` (boolean, required): true if the page was reloaded and re-inspected after the action, confirming the block is actually visible/present
- `account_used` (string | null, optional): handle of the logged-in account that performed the action, read from the account switcher UI (not assumed from input)

## FAQ

### What does "Block X user" do?

Block an X user by handle. Already-blocked accounts are reported rather than re-blocked. Returns handle, blocked, was_blocked.

### How do I automatically block X user on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/block_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/block_user

### Is there a x.com API to block X user?

You do not need one. "Block X user" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: handle.

### What does it return?

It returns handle, blocked, was_blocked, account_used, verified_on_page.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/block_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/block_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/block_user
