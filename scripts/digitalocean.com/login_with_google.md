# DigitalOcean login (Google SSO)

Log into DigitalOcean via 'Sign In with Google'. Auto-selects the sole signed-in account (no chooser), landing on cloud.digitalocean.com/dashboard; the chooser is still handled when shown. Only works when run through the browser extension, using the browser's native Google session — it does not work on managed/cloud browser runs.

- Site: digitalocean.com
- Address: `reduck/digitalocean.com/login_with_google`
- Updated: 2026-09-21 (v2)
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

Log into DigitalOcean via 'Sign In with Google'. Auto-selects the sole signed-in account (no chooser), landing on cloud.digitalocean.com/dashboard; the chooser is still handled when shown. Only works when run through the browser extension, using the browser's native Google session — it does not work on managed/cloud browser runs.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to digitalocean.com?

No. It only uses pages of digitalocean.com that are reachable without signing in.

### Does it change anything on digitalocean.com, or only read data?

It makes changes on digitalocean.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/digitalocean.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/digitalocean.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/digitalocean.com/login_with_google
