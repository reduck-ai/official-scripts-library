# Product Hunt login (Google SSO)

Log into Product Hunt with its Google sign-in option, handling the Google account chooser and consent screen. Returns straight away if you are already signed in, and reports the Product Hunt handle, display name and user id. Optionally pass which Google account to use. Needs a browser already signed in to Google and a Google account that already has a Product Hunt account.

- Site: producthunt.com
- Address: `reduck/producthunt.com/login_with_google`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/producthunt.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/producthunt.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account listed.

## Output

- `url` (string, required)
- `already` (boolean, required): true when a session already existed and no sign-in was needed
- `loggedIn` (boolean, required)
- `name` (string | null, optional): Product Hunt display name
- `userId` (string | null, optional)
- `username` (string | null, optional): Product Hunt handle, without the @

## FAQ

### What does "Product Hunt login (Google SSO)" do?

Log into Product Hunt with its Google sign-in option, handling the Google account chooser and consent screen. Returns straight away if you are already signed in, and reports the Product Hunt handle, display name and user id. Optionally pass which Google account to use. Needs a browser already signed in to Google and a Google account that already has a Product Hunt account.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, name, userId, already, loggedIn, username.

### Do I need to be logged in to producthunt.com?

Yes. It acts as you on producthunt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the producthunt.com cookies saved by the Reduck extension.

### Does it change anything on producthunt.com, or only read data?

It makes changes on producthunt.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/producthunt.com/login_with_google
