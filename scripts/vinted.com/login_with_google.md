# Vinted login (Google SSO)

Log into Vinted with Continue with Google on the country site where your account lives (vinted.fr by default; pass `domain`, e.g. www.vinted.com), handling the Google account chooser and consent screen. Declines non-essential cookies on the banner. Returns straight away if you are already signed in, and reports the Vinted account email. If the Google account has no Vinted account on that site, it stops instead of signing up; a captcha is named rather than attempted. Needs a browser already signed in to Google.

- Site: vinted.com
- Address: `reduck/vinted.com/login_with_google`
- Updated: 2026-09-30 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/vinted.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/vinted.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account listed.
- `domain` (string, optional): Vinted country site the account lives on, e.g. "www.vinted.fr" (default) or "www.vinted.com". Vinted accounts are per country site: sign in where the account exists.

## Output

- `url` (string, required)
- `already` (boolean, required): true when a session already existed and no sign-in was needed
- `loggedIn` (boolean, required)
- `domain` (string, optional)
- `account` (string | null, optional): Vinted account email

## FAQ

### What does "Vinted login (Google SSO)" do?

Log into Vinted with Continue with Google on the country site where your account lives (vinted.fr by default; pass `domain`, e.g. www.vinted.com), handling the Google account chooser and consent screen. Declines non-essential cookies on the banner. Returns straight away if you are already signed in, and reports the Vinted account email. If the Google account has no Vinted account on that site, it stops instead of signing up; a captcha is named rather than attempted. Needs a browser already signed in to Google.

### What information do I need to provide?

Optional: email, domain.

### What does it return?

It returns url, domain, account, already, loggedIn.

### Do I need to be logged in to vinted.com?

Yes. It acts as you on vinted.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the vinted.com cookies saved by the Reduck extension.

### Does it change anything on vinted.com, or only read data?

It makes changes on vinted.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/vinted.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vinted.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/vinted.com/login_with_google
