# Log in to Claude.ai with Google

Sign in to claude.ai with a Google account already signed in on this browser: picks the account (optional email argument), accepts the consent screen and lands in the app. Returns the signed-in account and the page reached; if the browser is already signed in to claude.ai it reports that account and changes nothing. Stops with a clear message when Google first asks for the account's password or a 2-step check, or when the account is not signed in to Google here. Needs the browser extension, since it relies on the browser's own Google session.

- Site: claude.ai
- Address: `reduck/claude.ai/login_with_google`
- Updated: 2026-11-04 (v14)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Log in to Claude.ai with Google" do?

Sign in to claude.ai with a Google account already signed in on this browser: picks the account (optional email argument), accepts the consent screen and lands in the app. Returns the signed-in account and the page reached; if the browser is already signed in to claude.ai it reports that account and changes nothing. Stops with a clear message when Google first asks for the account's password or a 2-step check, or when the account is not signed in to Google here. Needs the browser extension, since it relies on the browser's own Google session.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to claude.ai?

No. It only uses pages of claude.ai that are reachable without signing in.

### Does it change anything on claude.ai, or only read data?

It makes changes on claude.ai, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/login_with_google
