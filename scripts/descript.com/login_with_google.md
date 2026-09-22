# Descript login (Google SSO)

Log into Descript via 'Continue with Google'. Drives the chooser and confirms the logged-in web.descript.com app shell. Only works when run through the browser extension, using the browser's native Google session — it does not work on managed/cloud browser runs.

- Site: descript.com
- Address: `reduck/descript.com/login_with_google`
- Updated: 2026-09-21 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/descript.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/descript.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Descript login (Google SSO)" do?

Log into Descript via 'Continue with Google'. Drives the chooser and confirms the logged-in web.descript.com app shell. Only works when run through the browser extension, using the browser's native Google session — it does not work on managed/cloud browser runs.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to descript.com?

No. It only uses pages of descript.com that are reachable without signing in.

### Does it change anything on descript.com, or only read data?

It makes changes on descript.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/descript.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/descript.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/descript.com/login_with_google
