# ngrok login (Google SSO)

Sign in to ngrok with a Google account and return the signed-in ngrok account. Returns at once when already signed in. Needs the paired browser, which holds the Google session. Pass email to pick an account; it fails by name when that account is not signed in to Google, when Google asks for a password, 2FA or passkey check (clear it once by hand, then re-run), or when the Google account has no ngrok account.

- Site: dashboard.ngrok.com
- Address: `reduck/dashboard.ngrok.com/login_with_google`
- Updated: 2026-10-20 (v8)
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

Sign in to ngrok with a Google account and return the signed-in ngrok account. Returns at once when already signed in. Needs the paired browser, which holds the Google session. Pass email to pick an account; it fails by name when that account is not signed in to Google, when Google asks for a password, 2FA or passkey check (clear it once by hand, then re-run), or when the Google account has no ngrok account.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to dashboard.ngrok.com?

No. It only uses pages of dashboard.ngrok.com that are reachable without signing in.

### Does it change anything on dashboard.ngrok.com, or only read data?

It makes changes on dashboard.ngrok.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dashboard.ngrok.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dashboard.ngrok.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dashboard.ngrok.com/login_with_google
