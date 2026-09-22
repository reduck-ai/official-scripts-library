# Cloudflare login (Google SSO)

Log into the Cloudflare dashboard via the Google button. Dismisses the cookie banner, handles a remembered-account quick sign-in if one exists, drives the chooser, and lands on the dashboard. Best run on your own paired browser rather than a freshly launched one, since it relies on an existing Google session. Known limitation: if Cloudflare forces a 2FA or passkey step-up on the Google redirect, the login can't complete unattended — verify that step manually once in the same browser, then re-run. Optional `email` arg picks which Google account to use.

- Site: cloudflare.com
- Address: `reduck/cloudflare.com/login_with_google`
- Updated: 2026-08-24 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cloudflare.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Cloudflare login (Google SSO)" do?

Log into the Cloudflare dashboard via the Google button. Dismisses the cookie banner, handles a remembered-account quick sign-in if one exists, drives the chooser, and lands on the dashboard. Best run on your own paired browser rather than a freshly launched one, since it relies on an existing Google session. Known limitation: if Cloudflare forces a 2FA or passkey step-up on the Google redirect, the login can't complete unattended — verify that step manually once in the same browser, then re-run. Optional `email` arg picks which Google account to use.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to cloudflare.com?

No. It only uses pages of cloudflare.com that are reachable without signing in.

### Does it change anything on cloudflare.com, or only read data?

It makes changes on cloudflare.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cloudflare.com/login_with_google
