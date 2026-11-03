# Google Calendar whoami (signed-in account)

Report which Google account Google Calendar is signed in as in this browser: display name and email. When the browser is signed out, it fails with a sign-in error that says to sign in and retry.

- Site: calendar.google.com
- Address: `reduck/calendar.google.com/whoami`
- Updated: 2026-11-02 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendar.google.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/whoami
```

## Input

- `account` (string, optional): Which signed-in Google account to report: its email, or its number in this browser ("1"), as mail.google.com/list_accounts lists them. The run fails if that account is not signed in. Omit for the first signed-in account.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `authuser` (integer | null, optional): The account's number in this browser (/calendar/u/<n>/).

## FAQ

### What does "Google Calendar whoami (signed-in account)" do?

Report which Google account Google Calendar is signed in as in this browser: display name and email. When the browser is signed out, it fails with a sign-in error that says to sign in and retry.

### What information do I need to provide?

Optional: account.

### What does it return?

It returns name, email, authuser, loggedIn.

### Do I need to be logged in to calendar.google.com?

Yes. It acts as you on calendar.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendar.google.com cookies saved by the Reduck extension.

### Does it change anything on calendar.google.com, or only read data?

It only reads. It looks things up on calendar.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendar.google.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendar.google.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendar.google.com/whoami
