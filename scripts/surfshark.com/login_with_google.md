# Surfshark login (Google SSO)

Log into your Surfshark account with Google sign-in, handling the cookie banner, the Google account chooser and the confirm screen, and land on the account dashboard. Returns straight away if already signed in, and reports the account email. Optionally pass which Google account to use.

- Site: surfshark.com
- Address: `reduck/surfshark.com/login_with_google`
- Updated: 2026-10-02 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/surfshark.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/surfshark.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account listed.

## Output

- `url` (string, required)
- `already` (boolean, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Surfshark login (Google SSO)" do?

Log into your Surfshark account with Google sign-in, handling the cookie banner, the Google account chooser and the confirm screen, and land on the account dashboard. Returns straight away if already signed in, and reports the account email. Optionally pass which Google account to use.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, already, loggedIn.

### Do I need to be logged in to surfshark.com?

No. It only uses pages of surfshark.com that are reachable without signing in.

### Does it change anything on surfshark.com, or only read data?

It makes changes on surfshark.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/surfshark.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/surfshark.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/surfshark.com/login_with_google
