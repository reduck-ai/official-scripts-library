# Trello login

Log into Trello via Google SSO (through Atlassian identity). Drives the sign-in flow and lands on your boards.

- Site: trello.com
- Address: `reduck/trello.com/login_with_google`
- Updated: 2026-08-21 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/trello.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/trello.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)
- `already_signed_in` (boolean, optional): The session was already authenticated, so no SSO round-trip was needed.

## FAQ

### What does "Trello login" do?

Log into Trello via Google SSO (through Atlassian identity). Drives the sign-in flow and lands on your boards.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn, already_signed_in.

### Do I need to be logged in to trello.com?

Yes. It acts as you on trello.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the trello.com cookies saved by the Reduck extension.

### Does it change anything on trello.com, or only read data?

It makes changes on trello.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/trello.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trello.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/trello.com/login_with_google
