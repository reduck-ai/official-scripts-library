# HubSpot login (Google SSO)

Log into HubSpot (app.hubspot.com) with Google SSO: submits your email, signs in through Google, and handles the account chooser and first-time consent. HubSpot then shows a new-device email-verification step: pass the 6-digit code as `code`, or sign in once manually so HubSpot trusts the device — that confirmation is reliable only on a trusted device, so in practice this re-logs you in after one manual sign-in. `email` is required for a fresh sign-in: HubSpot's login is identifier-first, so the Google option only appears once an email is submitted, and it also selects which Google account to use.

- Site: app.hubspot.com
- Address: `reduck/app.hubspot.com/login_with_google`
- Updated: 2026-08-24 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.hubspot.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/login_with_google
```

## Input

- `code` (string, optional): 6-digit HubSpot log-in code from the email HubSpot sends when it does not recognise the device. Not needed on a device HubSpot already trusts, or when the browser already has a live HubSpot session.
- `email` (string, optional): Google account to sign in with (e.g. you@company.com). Required when a fresh sign-in is needed: HubSpot's login is identifier-first, so the Google button only renders after an email is submitted. Ignored when the browser is already signed in, so it's optional overall.

## Output

- `url` (string, required): The HubSpot URL the run ended on, an app or portal-chooser route, never /login or /login/confirm-to-login.
- `step` (string, required): already when the browser already had a live HubSpot session, code when a device-confirmation code was entered, sso when Google SSO alone was enough.
- `loggedIn` (boolean, required): Always true on a successful return, a run that cannot sign in throws instead.
- `note` (string | null, optional)
- `account` (string | null, optional): The Google account the SSO flow was driven with. Null on the already path.

## FAQ

### What does "HubSpot login (Google SSO)" do?

Log into HubSpot (app.hubspot.com) with Google SSO: submits your email, signs in through Google, and handles the account chooser and first-time consent. HubSpot then shows a new-device email-verification step: pass the 6-digit code as `code`, or sign in once manually so HubSpot trusts the device — that confirmation is reliable only on a trusted device, so in practice this re-logs you in after one manual sign-in. `email` is required for a fresh sign-in: HubSpot's login is identifier-first, so the Google option only appears once an email is submitted, and it also selects which Google account to use.

### What information do I need to provide?

Optional: code, email.

### What does it return?

It returns url, note, step, account, loggedIn.

### Do I need to be logged in to app.hubspot.com?

Yes. It acts as you on app.hubspot.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.hubspot.com cookies saved by the Reduck extension.

### Does it change anything on app.hubspot.com, or only read data?

It makes changes on app.hubspot.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.hubspot.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.hubspot.com/login_with_google
