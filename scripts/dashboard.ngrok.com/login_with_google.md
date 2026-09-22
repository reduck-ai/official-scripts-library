# ngrok login (Google SSO)

Log into the ngrok dashboard via the "Log in with Google" button. Drives the Google account chooser (and consent screen if one appears) and lands on dashboard.ngrok.com. If already signed in, returns immediately. Requires running on the extension-paired browser rather than a managed/cloud browser. If Google requires a step-up (password re-confirm, 2FA, or passkey), that has to be cleared manually before this can complete — re-run afterward. Optional `email` arg picks which account row to use in the chooser; omit for the first row.

- Site: dashboard.ngrok.com
- Address: `reduck/dashboard.ngrok.com/login_with_google`
- Updated: 2026-08-20 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dashboard.ngrok.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dashboard.ngrok.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser (e.g. name@domain.com). Omit to use the first/only account row.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "ngrok login (Google SSO)" do?

Log into the ngrok dashboard via the "Log in with Google" button. Drives the Google account chooser (and consent screen if one appears) and lands on dashboard.ngrok.com. If already signed in, returns immediately. Requires running on the extension-paired browser rather than a managed/cloud browser. If Google requires a step-up (password re-confirm, 2FA, or passkey), that has to be cleared manually before this can complete — re-run afterward. Optional `email` arg picks which account row to use in the chooser; omit for the first row.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to dashboard.ngrok.com?

No. It only uses pages of dashboard.ngrok.com that are reachable without signing in.

### Does it change anything on dashboard.ngrok.com, or only read data?

It makes changes on dashboard.ngrok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dashboard.ngrok.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dashboard.ngrok.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dashboard.ngrok.com/login_with_google
