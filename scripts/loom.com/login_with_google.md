# Loom login

Sign in to Loom with your Google account and land in your Loom video library, confirming which account the session actually belongs to. If the browser is already signed in, it says so instead of signing in again — and tells you when it is signed in as someone other than the account you asked for. When Loom cannot complete the sign-in because the account has no workspace yet, or Google has no matching account to offer, it stops with a message naming exactly what is missing rather than joining a team on your behalf.

- Site: loom.com
- Address: `reduck/loom.com/login_with_google`
- Updated: 2026-08-21 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/loom.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/loom.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Loom login" do?

Sign in to Loom with your Google account and land in your Loom video library, confirming which account the session actually belongs to. If the browser is already signed in, it says so instead of signing in again — and tells you when it is signed in as someone other than the account you asked for. When Loom cannot complete the sign-in because the account has no workspace yet, or Google has no matching account to offer, it stops with a message naming exactly what is missing rather than joining a team on your behalf.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to loom.com?

Yes. It acts as you on loom.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the loom.com cookies saved by the Reduck extension.

### Does it change anything on loom.com, or only read data?

It makes changes on loom.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/loom.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/loom.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/loom.com/login_with_google
