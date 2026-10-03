# Dropcontact login (Google SSO)

Log into Dropcontact with Log In with Google, handling the Google account chooser and consent screen, and land on your Dropcontact dashboard. Returns straight away if you are already signed in, and reports the Dropcontact account. Optionally pass which Google account to use. Needs a browser that is already signed in to Google.

- Site: dropcontact.com
- Address: `reduck/dropcontact.com/login_with_google`
- Updated: 2026-10-02 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dropcontact.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dropcontact.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account listed.

## Output

- `url` (string, required)
- `already` (boolean, required): true when a session already existed and no sign-in was needed
- `loggedIn` (boolean, required)
- `account` (string | null, optional)
- `workspace` (string | null, optional)

## FAQ

### What does "Dropcontact login (Google SSO)" do?

Log into Dropcontact with Log In with Google, handling the Google account chooser and consent screen, and land on your Dropcontact dashboard. Returns straight away if you are already signed in, and reports the Dropcontact account. Optionally pass which Google account to use. Needs a browser that is already signed in to Google.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, already, loggedIn, workspace.

### Do I need to be logged in to dropcontact.com?

No. It only uses pages of dropcontact.com that are reachable without signing in.

### Does it change anything on dropcontact.com, or only read data?

It makes changes on dropcontact.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dropcontact.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dropcontact.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dropcontact.com/login_with_google
