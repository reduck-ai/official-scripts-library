# Atlassian login

Log into Atlassian via Google sign-in — clicks the Google option, picks the account (optional email arg), clears any consent screen, and lands in an Atlassian product. Best run on your own paired browser rather than a freshly launched one, since it relies on an existing Google session in that browser.

- Site: atlassian.com
- Address: `reduck/atlassian.com/login_with_google`
- Updated: 2026-08-24 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/atlassian.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/atlassian.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Atlassian login" do?

Log into Atlassian via Google sign-in — clicks the Google option, picks the account (optional email arg), clears any consent screen, and lands in an Atlassian product. Best run on your own paired browser rather than a freshly launched one, since it relies on an existing Google session in that browser.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to atlassian.com?

No. It only uses pages of atlassian.com that are reachable without signing in.

### Does it change anything on atlassian.com, or only read data?

It makes changes on atlassian.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/atlassian.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/atlassian.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/atlassian.com/login_with_google
