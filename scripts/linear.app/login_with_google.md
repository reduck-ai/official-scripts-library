# Linear login (Google SSO)

Log into Linear via "Continue with Google", using your browser's own signed-in Google account. Drives the account chooser and consent screen, then lands you on your workspace. Requires the local browser extension — not available in cloud/managed runs.

- Site: linear.app
- Address: `reduck/linear.app/login_with_google`
- Updated: 2026-08-28 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linear.app/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linear.app/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Linear login (Google SSO)" do?

Log into Linear via "Continue with Google", using your browser's own signed-in Google account. Drives the account chooser and consent screen, then lands you on your workspace. Requires the local browser extension — not available in cloud/managed runs.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to linear.app?

No. It only uses pages of linear.app that are reachable without signing in.

### Does it change anything on linear.app, or only read data?

It makes changes on linear.app, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linear.app/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linear.app/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linear.app/login_with_google
