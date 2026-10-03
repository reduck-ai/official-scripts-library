# lemlist login (Google SSO)

Log into lemlist with Google sign-in, handling the Google account chooser and consent screen. Returns straight away if already signed in, and reports the lemlist account. Optionally pass which Google account to use. Needs a browser already signed in to Google and a Google account that is already a lemlist user.

- Site: lemlist.com
- Address: `reduck/lemlist.com/login_with_google`
- Updated: 2026-10-02 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lemlist.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lemlist.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account listed.

## Output

- `url` (string, required)
- `already` (boolean, required): true when a session already existed and no sign-in was needed
- `loggedIn` (boolean, required)
- `userId` (string | null, optional)
- `account` (string | null, optional): lemlist user email

## FAQ

### What does "lemlist login (Google SSO)" do?

Log into lemlist with Google sign-in, handling the Google account chooser and consent screen. Returns straight away if already signed in, and reports the lemlist account. Optionally pass which Google account to use. Needs a browser already signed in to Google and a Google account that is already a lemlist user.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, userId, account, already, loggedIn.

### Do I need to be logged in to lemlist.com?

No. It only uses pages of lemlist.com that are reachable without signing in.

### Does it change anything on lemlist.com, or only read data?

It makes changes on lemlist.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lemlist.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lemlist.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/lemlist.com/login_with_google
