# Neon login (Google SSO)

Log into the Neon console via Google OAuth (through Neon's Keycloak): clicks Google and lands on your Neon projects. Skips straight to your projects if you're already signed in.

- Site: console.neon.tech
- Address: `reduck/console.neon.tech/login_with_google`
- Updated: 2026-08-20 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.neon.tech/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/login_with_google
```

## Input

- `email` (string, optional): Google account to pick if Google shows an account chooser. Omit to use the single signed-in account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Neon login (Google SSO)" do?

Log into the Neon console via Google OAuth (through Neon's Keycloak): clicks Google and lands on your Neon projects. Skips straight to your projects if you're already signed in.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to console.neon.tech?

Yes. It acts as you on console.neon.tech: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the console.neon.tech cookies saved by the Reduck extension.

### Does it change anything on console.neon.tech, or only read data?

It makes changes on console.neon.tech, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.neon.tech/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/console.neon.tech/login_with_google
