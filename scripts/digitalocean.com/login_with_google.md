# DigitalOcean login (Google SSO)

Log into DigitalOcean with Sign in with Google, picking the given Google account, and land on your DigitalOcean dashboard. Returns straight away if you are already signed in, and reports the signed-in account. Needs a browser already signed in to that Google account; it works through the browser extension, not on a managed browser.

- Site: digitalocean.com
- Address: `reduck/digitalocean.com/login_with_google`
- Updated: 2026-11-23 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/digitalocean.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/digitalocean.com/login_with_google
```

## Input

- `email` (string, optional)

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "DigitalOcean login (Google SSO)" do?

Log into DigitalOcean with Sign in with Google, picking the given Google account, and land on your DigitalOcean dashboard. Returns straight away if you are already signed in, and reports the signed-in account. Needs a browser already signed in to that Google account; it works through the browser extension, not on a managed browser.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to digitalocean.com?

No. It only uses pages of digitalocean.com that are reachable without signing in.

### Does it change anything on digitalocean.com, or only read data?

It makes changes on digitalocean.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/digitalocean.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/digitalocean.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/digitalocean.com/login_with_google
