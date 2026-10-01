# Browserbase login (Google SSO)

Log into Browserbase with Continue with Google, picking the given Google account, and land on the Browserbase dashboard. Returns straight away if already signed in, and reports the account Browserbase itself is signed in as, never an echo of the argument. Needs the extension-paired browser with that Google account signed in. Warning: if the Google account has no Browserbase account yet, Browserbase creates one (with a new organization) silently during sign-in — there is no sign-up step to stop at.

- Site: browserbase.com
- Address: `reduck/browserbase.com/login_with_google`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/browserbase.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/browserbase.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser (e.g. name@domain.com). Omit to use the first account row.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional): The signed-in Browserbase account's primary email, as Clerk reports it — never an echo of the email argument.

## FAQ

### What does "Browserbase login (Google SSO)" do?

Log into Browserbase with Continue with Google, picking the given Google account, and land on the Browserbase dashboard. Returns straight away if already signed in, and reports the account Browserbase itself is signed in as, never an echo of the argument. Needs the extension-paired browser with that Google account signed in. Warning: if the Google account has no Browserbase account yet, Browserbase creates one (with a new organization) silently during sign-in — there is no sign-up step to stop at.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to browserbase.com?

No. It only uses pages of browserbase.com that are reachable without signing in.

### Does it change anything on browserbase.com, or only read data?

It makes changes on browserbase.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/browserbase.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/browserbase.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/browserbase.com/login_with_google
