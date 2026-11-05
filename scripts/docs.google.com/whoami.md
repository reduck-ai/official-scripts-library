# Google Docs whoami (signed-in account)

Report which Google account Google Docs/Sheets is signed in as in this browser: display name and email. When the browser is signed out, the run fails with a signed-out error that says to sign in to Google Docs and retry.

- Site: docs.google.com
- Address: `reduck/docs.google.com/whoami`
- Updated: 2026-11-04 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional): The account Google Docs uses when no account is chosen.
- `email` (string | null, optional): The account Google Docs uses when no account is chosen: the one the Docs scripts act as without an account argument.
- `accounts` (array, optional): Every Google account signed in to this browser, by its index (u/0, u/1, ...). Pass an email as account to the Docs scripts to act as another one.

## FAQ

### What does "Google Docs whoami (signed-in account)" do?

Report which Google account Google Docs/Sheets is signed in as in this browser: display name and email. When the browser is signed out, the run fails with a signed-out error that says to sign in to Google Docs and retry.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, accounts, loggedIn.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It only reads. It looks things up on docs.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/whoami
