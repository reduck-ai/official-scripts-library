# Attio login (Google SSO)

Log into the Attio CRM with Sign in with Google, handling the Google account chooser and consent screen, and land in your Attio workspace. Returns straight away if you are already signed in, and reports the workspace it opened. Optionally pass which Google account to use. Needs a browser that is already signed in to Google.

- Site: attio.com
- Address: `reduck/attio.com/login_with_google`
- Updated: 2026-09-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/attio.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/attio.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account listed.

## Output

- `url` (string, required)
- `already` (boolean, required): true when a session already existed and no sign-in was needed
- `loggedIn` (boolean, required)
- `account` (string | null, optional): Always null: Attio exposes the workspace, not the signed-in email, without extra lookups
- `workspace` (string | null, optional): Attio workspace slug

## FAQ

### What does "Attio login (Google SSO)" do?

Log into the Attio CRM with Sign in with Google, handling the Google account chooser and consent screen, and land in your Attio workspace. Returns straight away if you are already signed in, and reports the workspace it opened. Optionally pass which Google account to use. Needs a browser that is already signed in to Google.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, already, loggedIn, workspace.

### Do I need to be logged in to attio.com?

Yes. It acts as you on attio.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the attio.com cookies saved by the Reduck extension.

### Does it change anything on attio.com, or only read data?

It makes changes on attio.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/attio.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/attio.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/attio.com/login_with_google
