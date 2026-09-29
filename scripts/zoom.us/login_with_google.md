# Zoom login (Google SSO)

Log into Zoom (zoom.us) with Sign in with Google, picking the given Google account, and land on the Zoom profile page. Returns straight away if already signed in, and reports the account Zoom itself shows, never an echo of the argument. Never creates an account: if the Google account has no Zoom account, Zoom's sign-up / activation / birthday screen stops the run with a named error. Needs the extension-paired browser with that Google account signed in.

- Site: zoom.us
- Address: `reduck/zoom.us/login_with_google`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/zoom.us/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/zoom.us/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account row.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional): The signed-in account's email as the site shows it on its own profile page, never an echo of the email argument.

## FAQ

### What does "Zoom login (Google SSO)" do?

Log into Zoom (zoom.us) with Sign in with Google, picking the given Google account, and land on the Zoom profile page. Returns straight away if already signed in, and reports the account Zoom itself shows, never an echo of the argument. Never creates an account: if the Google account has no Zoom account, Zoom's sign-up / activation / birthday screen stops the run with a named error. Needs the extension-paired browser with that Google account signed in.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to zoom.us?

No. It only uses pages of zoom.us that are reachable without signing in.

### Does it change anything on zoom.us, or only read data?

It makes changes on zoom.us, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/zoom.us/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zoom.us/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/zoom.us/login_with_google
