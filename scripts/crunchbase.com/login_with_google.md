# Crunchbase login (Google SSO)

Log into Crunchbase with Continue with Google, using a Google account already signed in on this browser. Returns straight away if you are already signed in, and reports the Crunchbase account. It only signs in to an existing Crunchbase account and never creates one. Crunchbase allows one device at a time, so signing in here signs the account out elsewhere.

- Site: crunchbase.com
- Address: `reduck/crunchbase.com/login_with_google`
- Updated: 2026-10-05 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crunchbase.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account listed.

## Output

- `url` (string, required)
- `already` (boolean, required): true when a session already existed and no sign-in was needed
- `loggedIn` (boolean, required)
- `account` (string | null, optional): Crunchbase account email

## FAQ

### What does "Crunchbase login (Google SSO)" do?

Log into Crunchbase with Continue with Google, using a Google account already signed in on this browser. Returns straight away if you are already signed in, and reports the Crunchbase account. It only signs in to an existing Crunchbase account and never creates one. Crunchbase allows one device at a time, so signing in here signs the account out elsewhere.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, already, loggedIn.

### Do I need to be logged in to crunchbase.com?

No. It only uses pages of crunchbase.com that are reachable without signing in.

### Does it change anything on crunchbase.com, or only read data?

It makes changes on crunchbase.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/crunchbase.com/login_with_google
