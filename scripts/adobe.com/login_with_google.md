# Adobe login (Google SSO)

Log into Adobe with Google.

- Site: adobe.com
- Address: `reduck/adobe.com/login_with_google`
- Updated: 2026-09-30 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/adobe.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/adobe.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account row.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional): The signed-in account's email as the site shows it on its own profile page, never an echo of the email argument.

## FAQ

### What does "Adobe login (Google SSO)" do?

Log into Adobe with Google.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to adobe.com?

No. It only uses pages of adobe.com that are reachable without signing in.

### Does it change anything on adobe.com, or only read data?

It makes changes on adobe.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/adobe.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/adobe.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/adobe.com/login_with_google
