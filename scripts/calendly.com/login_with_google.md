# Calendly login

Log into Calendly via Google SSO (same-tab redirect). Picks the account (optional email arg), clears consent, and lands in the Calendly app. Requires a browser with an existing Google sign-in — does not work in hosted/cloud browser environments.

- Site: calendly.com
- Address: `reduck/calendly.com/login_with_google`
- Updated: 2026-08-21 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendly.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendly.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first/only account.

## Output

- `url` (string, required): The Calendly app URL the run ended on. Never a /login or /signup route — a run that ends there throws instead.
- `loggedIn` (boolean, required): Always true on a successful return: the run confirms the session by re-requesting an app route and checking it does not bounce to login. A run that cannot sign in throws rather than returning false.
- `account` (string | null, optional): The Google identity the SSO was driven with (the `email` argument, or the address read off the chooser row that was clicked). This is the Google account used, not a Calendly account read back from the app — Calendly surfaces no account email on the pages this script visits.

## FAQ

### What does "Calendly login" do?

Log into Calendly via Google SSO (same-tab redirect). Picks the account (optional email arg), clears consent, and lands in the Calendly app. Requires a browser with an existing Google sign-in — does not work in hosted/cloud browser environments.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to calendly.com?

Yes. It acts as you on calendly.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendly.com cookies saved by the Reduck extension.

### Does it change anything on calendly.com, or only read data?

It makes changes on calendly.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendly.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendly.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendly.com/login_with_google
