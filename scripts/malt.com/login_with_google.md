# Malt login (Google SSO)

Log into Malt with Google sign-in, handling Google's account chooser and consent screen, and land on your Malt dashboard. Returns straight away if this browser is already signed in, and reports the Malt account email. Optionally pass which Google account to use. Stops instead of creating a new Malt account.

- Site: malt.com
- Address: `reduck/malt.com/login_with_google`
- Updated: 2026-10-02 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/malt.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/malt.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account listed.

## Output

- `url` (string, required)
- `already` (boolean, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional): Malt account email

## FAQ

### What does "Malt login (Google SSO)" do?

Log into Malt with Google sign-in, handling Google's account chooser and consent screen, and land on your Malt dashboard. Returns straight away if this browser is already signed in, and reports the Malt account email. Optionally pass which Google account to use. Stops instead of creating a new Malt account.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, already, loggedIn.

### Do I need to be logged in to malt.com?

No. It only uses pages of malt.com that are reachable without signing in.

### Does it change anything on malt.com, or only read data?

It makes changes on malt.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/malt.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/malt.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/malt.com/login_with_google
