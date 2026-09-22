# Surfshark login (Google SSO)

Log into Surfshark (my.surfshark.com) via Google SSO: dismisses the cookie banner, drives the OAuth redirect (account chooser + consent confirm) and lands on the account dashboard.

- Site: my.surfshark.com
- Address: `reduck/my.surfshark.com/login_with_google`
- Updated: 2026-08-20 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/my.surfshark.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/my.surfshark.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional)

## FAQ

### What does "Surfshark login (Google SSO)" do?

Log into Surfshark (my.surfshark.com) via Google SSO: dismisses the cookie banner, drives the OAuth redirect (account chooser + consent confirm) and lands on the account dashboard.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to my.surfshark.com?

Yes. It acts as you on my.surfshark.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the my.surfshark.com cookies saved by the Reduck extension.

### Does it change anything on my.surfshark.com, or only read data?

It makes changes on my.surfshark.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/my.surfshark.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/my.surfshark.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/my.surfshark.com/login_with_google
