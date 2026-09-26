# Reddit login (emailed one-time link via Gmail)

Sign in to Reddit without a password: requests Reddit's emailed one-time login link for the given address, opens it from that address's Gmail inbox in the same browser, and lands signed in. Returns straight away if already signed in, and reports the Reddit username. The Gmail account for that address must be signed in on this browser.

- Site: reddit.com
- Address: `reduck/reddit.com/login`
- Updated: 2026-09-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/login`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/login
```

## Input

- `email` (string, required): Email address of the Reddit account; its Gmail inbox must be signed in on this browser.

## Output

- `already` (boolean, required)
- `loggedIn` (boolean, required)
- `username` (string | null, optional)

## FAQ

### What does "Reddit login (emailed one-time link via Gmail)" do?

Sign in to Reddit without a password: requests Reddit's emailed one-time login link for the given address, opens it from that address's Gmail inbox in the same browser, and lands signed in. Returns straight away if already signed in, and reports the Reddit username. The Gmail account for that address must be signed in on this browser.

### What information do I need to provide?

Required: email.

### What does it return?

It returns already, loggedIn, username.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It makes changes on reddit.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/login, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/login

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/login
