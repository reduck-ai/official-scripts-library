# Miro login (Google SSO)

Log into Miro with your Google account and land on the boards dashboard. Returns straight away if you're already signed in, so it's safe to run repeatedly.

- Site: miro.com
- Address: `reduck/miro.com/login_with_google`
- Updated: 2026-08-21 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/miro.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/miro.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick if Google shows an account chooser. Omit to use the single signed-in account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Miro login (Google SSO)" do?

Log into Miro with your Google account and land on the boards dashboard. Returns straight away if you're already signed in, so it's safe to run repeatedly.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to miro.com?

Yes. It acts as you on miro.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the miro.com cookies saved by the Reduck extension.

### Does it change anything on miro.com, or only read data?

It makes changes on miro.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/miro.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/miro.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/miro.com/login_with_google
