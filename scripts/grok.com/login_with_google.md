# Grok login (Google SSO)

Log into Grok with Continue with Google, handling the Google account chooser and consent screen. Returns straight away if you are already signed in, and reports the Grok account email. Stops with a clear message instead of signing up if the Google account has no Grok account yet. Optionally pass which Google account to use. Needs a browser already signed in to Google.

- Site: grok.com
- Address: `reduck/grok.com/login_with_google`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/grok.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/grok.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account listed.

## Output

- `url` (string, required)
- `already` (boolean, required): true when a session already existed and no sign-in was needed
- `loggedIn` (boolean, required)
- `account` (string | null, optional): Grok account email

## FAQ

### What does "Grok login (Google SSO)" do?

Log into Grok with Continue with Google, handling the Google account chooser and consent screen. Returns straight away if you are already signed in, and reports the Grok account email. Stops with a clear message instead of signing up if the Google account has no Grok account yet. Optionally pass which Google account to use. Needs a browser already signed in to Google.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, already, loggedIn.

### Do I need to be logged in to grok.com?

Yes. It acts as you on grok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the grok.com cookies saved by the Reduck extension.

### Does it change anything on grok.com, or only read data?

It makes changes on grok.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/grok.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/grok.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/grok.com/login_with_google
