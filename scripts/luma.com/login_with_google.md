# Luma login (Google SSO)

Log into Luma with Sign in with Google, handling the Google account chooser and consent screen (Luma runs it in a new tab) and skipping the passkey prompt, then land on your Luma home. Returns straight away if you are already signed in, and reports the Luma account email and name. Optionally pass which Google account to use. Needs a browser that is already signed in to Google.

- Site: luma.com
- Address: `reduck/luma.com/login_with_google`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/luma.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/luma.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account listed.

## Output

- `url` (string, required)
- `already` (boolean, required): true when a session already existed and no sign-in was needed
- `loggedIn` (boolean, required)
- `name` (string | null, optional): Luma display name
- `account` (string | null, optional): Luma account email

## FAQ

### What does "Luma login (Google SSO)" do?

Log into Luma with Sign in with Google, handling the Google account chooser and consent screen (Luma runs it in a new tab) and skipping the passkey prompt, then land on your Luma home. Returns straight away if you are already signed in, and reports the Luma account email and name. Optionally pass which Google account to use. Needs a browser that is already signed in to Google.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, name, account, already, loggedIn.

### Do I need to be logged in to luma.com?

Yes. It acts as you on luma.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the luma.com cookies saved by the Reduck extension.

### Does it change anything on luma.com, or only read data?

It makes changes on luma.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/luma.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/luma.com/login_with_google
