# Stripe Dashboard login (Google SSO)

Log into the Stripe Dashboard with Continue with Google, handling the Google account chooser and consent screen. Returns straight away if you are already signed in, and reports the Stripe user email. If Stripe asks for a two-step verification code it stops and says so instead of attempting it. Optionally pass which Google account to use. Needs a browser already signed in to Google and a Google account that is already a Stripe user.

- Site: dashboard.stripe.com
- Address: `reduck/dashboard.stripe.com/login_with_google`
- Updated: 2026-10-01 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dashboard.stripe.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dashboard.stripe.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account listed.

## Output

- `url` (string, required)
- `already` (boolean, required): true when a session already existed and no sign-in was needed
- `loggedIn` (boolean, required)
- `account` (string | null, optional): Stripe user email

## FAQ

### What does "Stripe Dashboard login (Google SSO)" do?

Log into the Stripe Dashboard with Continue with Google, handling the Google account chooser and consent screen. Returns straight away if you are already signed in, and reports the Stripe user email. If Stripe asks for a two-step verification code it stops and says so instead of attempting it. Optionally pass which Google account to use. Needs a browser already signed in to Google and a Google account that is already a Stripe user.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, already, loggedIn.

### Do I need to be logged in to dashboard.stripe.com?

Yes. It acts as you on dashboard.stripe.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dashboard.stripe.com cookies saved by the Reduck extension.

### Does it change anything on dashboard.stripe.com, or only read data?

It makes changes on dashboard.stripe.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dashboard.stripe.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dashboard.stripe.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dashboard.stripe.com/login_with_google
