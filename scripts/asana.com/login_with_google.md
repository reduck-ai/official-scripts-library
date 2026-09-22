# Asana login

Log into Asana via Google SSO. Picks the Google account (optional email arg), clears the Google consent screen, and lands in Asana. Requires an active Google session in the browser; not available on cloud/managed browsers.

- Site: asana.com
- Address: `reduck/asana.com/login_with_google`
- Updated: 2026-09-10 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/asana.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/asana.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account offered, or the existing Asana session if one is present.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Asana login" do?

Log into Asana via Google SSO. Picks the Google account (optional email arg), clears the Google consent screen, and lands in Asana. Requires an active Google session in the browser; not available on cloud/managed browsers.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to asana.com?

Yes. It acts as you on asana.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the asana.com cookies saved by the Reduck extension.

### Does it change anything on asana.com, or only read data?

It makes changes on asana.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/asana.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/asana.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/asana.com/login_with_google
