# Lucidchart login (Google SSO)

Log into Lucid (Lucidchart) using your connected Google account. Lands on the Lucid documents home; returns early if already signed in.

- Site: lucid.app
- Address: `reduck/lucid.app/login_with_google`
- Updated: 2026-08-20 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lucid.app/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lucid.app/login_with_google
```

## Input

- `email` (string, optional): Google account to pick if Google shows an account chooser. Omit to use the single signed-in account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Lucidchart login (Google SSO)" do?

Log into Lucid (Lucidchart) using your connected Google account. Lands on the Lucid documents home; returns early if already signed in.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to lucid.app?

Yes. It acts as you on lucid.app: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the lucid.app cookies saved by the Reduck extension.

### Does it change anything on lucid.app, or only read data?

It makes changes on lucid.app, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lucid.app/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lucid.app/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/lucid.app/login_with_google
