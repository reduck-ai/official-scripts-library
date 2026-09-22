# LinkedIn login

Log into LinkedIn via Google SSO. Drives LinkedIn's Continue-with-Google flow, picks the account (optional email arg), clears consent, and lands in the LinkedIn feed. Only works on a browser with its own signed-in Google session (not a managed or cloud browser).

- Site: linkedin.com
- Address: `reduck/linkedin.com/login_with_google`
- Updated: 2026-09-03 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first signed-in account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "LinkedIn login" do?

Log into LinkedIn via Google SSO. Drives LinkedIn's Continue-with-Google flow, picks the account (optional email arg), clears consent, and lands in the LinkedIn feed. Only works on a browser with its own signed-in Google session (not a managed or cloud browser).

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to linkedin.com?

No. It only uses pages of linkedin.com that are reachable without signing in.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/login_with_google
