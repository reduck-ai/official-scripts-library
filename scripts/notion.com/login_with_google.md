# Notion login (Google SSO)

Log into Notion via Google SSO, signing out first so the flow always runs fresh. Pass `email` to pick which Google account to use.

- Site: notion.com
- Address: `reduck/notion.com/login_with_google`
- Updated: 2026-08-07 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/notion.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/notion.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser (e.g. you@gmail.com). Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Notion login (Google SSO)" do?

Log into Notion via Google SSO, signing out first so the flow always runs fresh. Pass `email` to pick which Google account to use.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to notion.com?

Yes. It acts as you on notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the notion.com cookies saved by the Reduck extension.

### Does it change anything on notion.com, or only read data?

It makes changes on notion.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/notion.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/notion.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/notion.com/login_with_google
