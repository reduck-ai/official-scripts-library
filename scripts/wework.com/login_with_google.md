# WeWork login (Google SSO)

Log into WeWork Account Central using Sign in with Google, ending on the Account Central dashboard. Handles the Google account chooser and consent, and returns straight away if you are already signed in, so it is safe to run repeatedly. Optionally pass the Google account to use. Best run on your own paired browser rather than a freshly launched one, where the Google sign-in handshake can intermittently drop the tab partway through.

- Site: wework.com
- Address: `reduck/wework.com/login_with_google`
- Updated: 2026-09-04 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/wework.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/wework.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser (e.g. you@example.com). Omit for the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "WeWork login (Google SSO)" do?

Log into WeWork Account Central using Sign in with Google, ending on the Account Central dashboard. Handles the Google account chooser and consent, and returns straight away if you are already signed in, so it is safe to run repeatedly. Optionally pass the Google account to use. Best run on your own paired browser rather than a freshly launched one, where the Google sign-in handshake can intermittently drop the tab partway through.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to wework.com?

Yes. It acts as you on wework.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the wework.com cookies saved by the Reduck extension.

### Does it change anything on wework.com, or only read data?

It makes changes on wework.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/wework.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wework.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/wework.com/login_with_google
