# Cursor login (Google SSO)

Log into Cursor via "Continue with Google", driving the account chooser and landing on the Cursor dashboard. Requires running on the extension-paired browser rather than a managed/cloud browser.

- Site: cursor.com
- Address: `reduck/cursor.com/login_with_google`
- Updated: 2026-08-21 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cursor.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cursor.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Cursor login (Google SSO)" do?

Log into Cursor via "Continue with Google", driving the account chooser and landing on the Cursor dashboard. Requires running on the extension-paired browser rather than a managed/cloud browser.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to cursor.com?

No. It only uses pages of cursor.com that are reachable without signing in.

### Does it change anything on cursor.com, or only read data?

It makes changes on cursor.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cursor.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cursor.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cursor.com/login_with_google
