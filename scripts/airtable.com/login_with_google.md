# Airtable login

Log into Airtable via Google SSO, picking a specific account when an email is given. Only works on your own paired browser — it relies on that browser's own signed-in Google session rather than injected cookies.

- Site: airtable.com
- Address: `reduck/airtable.com/login_with_google`
- Updated: 2026-08-21 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/airtable.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/airtable.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Airtable login" do?

Log into Airtable via Google SSO, picking a specific account when an email is given. Only works on your own paired browser — it relies on that browser's own signed-in Google session rather than injected cookies.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to airtable.com?

No. It only uses pages of airtable.com that are reachable without signing in.

### Does it change anything on airtable.com, or only read data?

It makes changes on airtable.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/airtable.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airtable.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/airtable.com/login_with_google
