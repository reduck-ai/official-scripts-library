# Leboncoin login (Google SSO)

Log into Leboncoin with Continuer avec Google, handling the Google account chooser and consent screen, and land on your account page. Returns straight away if you are already signed in, and reports the Leboncoin account email. A captcha is named rather than attempted. Optionally pass which Google account to use. Needs a browser already signed in to Google and a Google account that already has a Leboncoin account.

- Site: leboncoin.fr
- Address: `reduck/leboncoin.fr/login_with_google`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leboncoin.fr/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account listed.

## Output

- `url` (string, required)
- `already` (boolean, required): true when a session already existed and no sign-in was needed
- `loggedIn` (boolean, required)
- `account` (string | null, optional): Leboncoin account email

## FAQ

### What does "Leboncoin login (Google SSO)" do?

Log into Leboncoin with Continuer avec Google, handling the Google account chooser and consent screen, and land on your account page. Returns straight away if you are already signed in, and reports the Leboncoin account email. A captcha is named rather than attempted. Optionally pass which Google account to use. Needs a browser already signed in to Google and a Google account that already has a Leboncoin account.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, already, loggedIn.

### Do I need to be logged in to leboncoin.fr?

Yes. It acts as you on leboncoin.fr: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the leboncoin.fr cookies saved by the Reduck extension.

### Does it change anything on leboncoin.fr, or only read data?

It makes changes on leboncoin.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/leboncoin.fr/login_with_google
