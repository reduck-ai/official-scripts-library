# Uber Eats login (Google SSO)

Log into Uber Eats with Continue with Google through Uber's sign-in, handling the Google account chooser and consent screen, and land on your orders page. Returns straight away if you are already signed in, and reports the Uber account name (and email when Uber Eats exposes it). Stops with a clear message if Uber asks for a phone number or SMS code instead of filling anything in. Needs a browser already signed in to Google and a Google account that already has an Uber account. Uber keeps rider and Eats sessions separate.

- Site: ubereats.com
- Address: `reduck/ubereats.com/login_with_google`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ubereats.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ubereats.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account listed.

## Output

- `url` (string, required)
- `already` (boolean, required): true when a session already existed and no sign-in was needed
- `loggedIn` (boolean, required)
- `name` (string | null, optional): Uber account first + last name
- `account` (string | null, optional): Uber account email when Uber Eats exposes it

## FAQ

### What does "Uber Eats login (Google SSO)" do?

Log into Uber Eats with Continue with Google through Uber's sign-in, handling the Google account chooser and consent screen, and land on your orders page. Returns straight away if you are already signed in, and reports the Uber account name (and email when Uber Eats exposes it). Stops with a clear message if Uber asks for a phone number or SMS code instead of filling anything in. Needs a browser already signed in to Google and a Google account that already has an Uber account. Uber keeps rider and Eats sessions separate.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, name, account, already, loggedIn.

### Do I need to be logged in to ubereats.com?

Yes. It acts as you on ubereats.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the ubereats.com cookies saved by the Reduck extension.

### Does it change anything on ubereats.com, or only read data?

It makes changes on ubereats.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ubereats.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ubereats.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ubereats.com/login_with_google
