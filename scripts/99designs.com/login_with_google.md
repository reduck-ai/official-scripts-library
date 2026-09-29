# 99designs login (Google SSO via Vista)

Log into 99designs (which signs in through a Vista account) with Continue with Google, picking the given Google account, and land on the 99designs account page (the country site, e.g. 99designs.fr). Returns straight away if already signed in, and reports the account 99designs itself shows. Never creates an account: a Vista / 99designs sign-up screen stops the run with a named error. Needs the extension-paired browser with that Google account signed in.

- Site: 99designs.com
- Address: `reduck/99designs.com/login_with_google`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/99designs.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/99designs.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account row.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional): The signed-in account as 99designs itself reports it (its full name, since the site renders no email), never an echo of the email argument.

## FAQ

### What does "99designs login (Google SSO via Vista)" do?

Log into 99designs (which signs in through a Vista account) with Continue with Google, picking the given Google account, and land on the 99designs account page (the country site, e.g. 99designs.fr). Returns straight away if already signed in, and reports the account 99designs itself shows. Never creates an account: a Vista / 99designs sign-up screen stops the run with a named error. Needs the extension-paired browser with that Google account signed in.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to 99designs.com?

No. It only uses pages of 99designs.com that are reachable without signing in.

### Does it change anything on 99designs.com, or only read data?

It makes changes on 99designs.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/99designs.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/99designs.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/99designs.com/login_with_google
