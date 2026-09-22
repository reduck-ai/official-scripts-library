# Unmute X user

Automatically unmute X user on x.com. Unmute an X user by handle. Accounts that aren't muted are reported rather than erroring. Returns handle, muted, was_muted.

- Site: x.com
- Address: `reduck/x.com/unmute_user`
- Updated: 2026-09-03 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/unmute_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/unmute_user
```

## Input

- `handle` (string, required): Target user's handle (with or without @).

## Output

- `muted` (boolean, required)
- `handle` (string, required)
- `was_muted` (boolean, required): already_present signal: true if muted before this call
- `verified_on_page` (boolean, required): true if the page was reloaded and re-inspected after the action, confirming the unmute is actually visible/present
- `account_used` (string | null, optional): handle of the logged-in account that performed the action, read from the account switcher UI (not assumed from input)

## FAQ

### What does "Unmute X user" do?

Unmute an X user by handle. Accounts that aren't muted are reported rather than erroring. Returns handle, muted, was_muted.

### How do I automatically unmute X user on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/unmute_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/unmute_user

### Is there a x.com API to unmute X user?

You do not need one. "Unmute X user" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: handle.

### What does it return?

It returns muted, handle, was_muted, account_used, verified_on_page.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/unmute_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/unmute_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/unmute_user
