# Claude (Anthropic) login

Log into Claude (Anthropic) via Google SSO. Drives Claude's Continue-with-Google popup, picks the account (optional email arg), clears the consent screen, and lands in the Claude app. Runs on your local extension-paired browser only — it relies on the browser's own signed-in Google session, so it won't work on a cloud/managed browser without one.

- Site: claude.ai
- Address: `reduck/claude.ai/login_with_google`
- Updated: 2026-08-24 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Claude (Anthropic) login" do?

Log into Claude (Anthropic) via Google SSO. Drives Claude's Continue-with-Google popup, picks the account (optional email arg), clears the consent screen, and lands in the Claude app. Runs on your local extension-paired browser only — it relies on the browser's own signed-in Google session, so it won't work on a cloud/managed browser without one.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It makes changes on claude.ai, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/login_with_google
