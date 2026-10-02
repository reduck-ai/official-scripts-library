# Postman login (Google SSO)

Log into Postman with Sign In with Google, handling the Google account chooser and consent screen (and Postman's own account chooser when several Postman sessions are known), and land on your account settings. Returns straight away if you are already signed in, and reports the Postman account email. Stops instead of signing up if the Google account has no Postman account. Optionally pass which account to use. Needs a browser already signed in to Google.

- Site: postman.co
- Address: `reduck/postman.co/login_with_google`
- Updated: 2026-10-01 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/postman.co/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/postman.co/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser (and Postman account to pick in Postman's own account chooser). Omit to use the first account listed.

## Output

- `url` (string, required)
- `already` (boolean, required): true when a session already existed and no sign-in was needed
- `loggedIn` (boolean, required)
- `account` (string | null, optional): Postman account email

## FAQ

### What does "Postman login (Google SSO)" do?

Log into Postman with Sign In with Google, handling the Google account chooser and consent screen (and Postman's own account chooser when several Postman sessions are known), and land on your account settings. Returns straight away if you are already signed in, and reports the Postman account email. Stops instead of signing up if the Google account has no Postman account. Optionally pass which account to use. Needs a browser already signed in to Google.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, already, loggedIn.

### Do I need to be logged in to postman.co?

Yes. It acts as you on postman.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the postman.co cookies saved by the Reduck extension.

### Does it change anything on postman.co, or only read data?

It makes changes on postman.co, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/postman.co/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/postman.co/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/postman.co/login_with_google
