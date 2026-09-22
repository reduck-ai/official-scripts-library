# Zapier login (Google SSO)

Log into Zapier using Sign in with Google, ending on the Zapier app home. Handles the Google account chooser and the confirmation step, and returns straight away if you are already signed in. Optionally pass which Google account to use.

- Site: zapier.com
- Address: `reduck/zapier.com/login_with_google`
- Updated: 2026-08-20 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/zapier.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/zapier.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Zapier login (Google SSO)" do?

Log into Zapier using Sign in with Google, ending on the Zapier app home. Handles the Google account chooser and the confirmation step, and returns straight away if you are already signed in. Optionally pass which Google account to use.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to zapier.com?

Yes. It acts as you on zapier.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the zapier.com cookies saved by the Reduck extension.

### Does it change anything on zapier.com, or only read data?

It makes changes on zapier.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/zapier.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zapier.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/zapier.com/login_with_google
