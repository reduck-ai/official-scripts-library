# Mistral login (Google SSO)

Log into the Mistral admin console (admin.mistral.ai) with Google SSO, handling the Google account chooser and the first-time consent screen, and land on the admin console. If you are already signed in, it returns immediately without repeating the login. Pass `email` to pick a specific Google account.

- Site: admin.mistral.ai
- Address: `reduck/admin.mistral.ai/login_with_google`
- Updated: 2026-08-28 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.mistral.ai/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.mistral.ai/login_with_google
```

## Input

- `email` (string, optional): Google account to pick if the chooser appears (e.g. you@company.com). Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Mistral login (Google SSO)" do?

Log into the Mistral admin console (admin.mistral.ai) with Google SSO, handling the Google account chooser and the first-time consent screen, and land on the admin console. If you are already signed in, it returns immediately without repeating the login. Pass `email` to pick a specific Google account.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to admin.mistral.ai?

Yes. It acts as you on admin.mistral.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.mistral.ai cookies saved by the Reduck extension.

### Does it change anything on admin.mistral.ai, or only read data?

It makes changes on admin.mistral.ai, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.mistral.ai/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.mistral.ai/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.mistral.ai/login_with_google
