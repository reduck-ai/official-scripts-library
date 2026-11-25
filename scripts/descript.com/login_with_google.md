# Descript login (Google SSO)

Sign in to Descript with Google, using the Google account already signed in to your browser (pick one with email when several are). Returns the Descript account that is now signed in. Works only on your own paired browser, not on a Reduck cloud browser.

- Site: descript.com
- Address: `reduck/descript.com/login_with_google`
- Updated: 2026-11-24 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/descript.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/descript.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Descript login (Google SSO)" do?

Sign in to Descript with Google, using the Google account already signed in to your browser (pick one with email when several are). Returns the Descript account that is now signed in. Works only on your own paired browser, not on a Reduck cloud browser.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to descript.com?

No. It only uses pages of descript.com that are reachable without signing in.

### Does it change anything on descript.com, or only read data?

It makes changes on descript.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/descript.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/descript.com/login_with_google

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/descript.com/login_with_google
