# GitHub login (Google SSO)

Log into GitHub via Google sign-in. Drives the account chooser and lands on your GitHub dashboard.

- Site: github.com
- Address: `reduck/github.com/login_with_google`
- Updated: 2026-08-21 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/github.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/github.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional): GitHub login handle read back from meta[name="user-login"] on the already-signed-in path, or the Google account picked in the chooser on a fresh sign-in.

## FAQ

### What does "GitHub login (Google SSO)" do?

Log into GitHub via Google sign-in. Drives the account chooser and lands on your GitHub dashboard.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to github.com?

Yes. It acts as you on github.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the github.com cookies saved by the Reduck extension.

### Does it change anything on github.com, or only read data?

It makes changes on github.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/github.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/github.com/login_with_google
