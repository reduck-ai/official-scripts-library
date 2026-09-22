# Hostinger login (Google SSO)

Log into Hostinger via Google sign-in and land on hPanel, returning the signed-in account read back from Hostinger itself rather than echoed from the request. If the browser already has a Hostinger session it returns straight away. Asking for an account other than the live session is refused by name instead of attempted, because Hostinger will not show its sign-in form while any session is open — sign out of hPanel first to switch accounts. Needs the extension-paired browser, not a managed/cloud one.

- Site: hostinger.com
- Address: `reduck/hostinger.com/login_with_google`
- Updated: 2026-08-21 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hostinger.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hostinger.com/login_with_google
```

## Input

- `email` (string, optional): Google account to sign in as. Omit to use whatever session the browser already has (or the first/only Google account when signing in fresh). If a Hostinger session for a different account is already open, the run is refused by name rather than attempted.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional): The signed-in Hostinger account, read back from the account profile hPanel itself loads. Null only when no address could be read — never an unverified echo of the `email` argument.

## FAQ

### What does "Hostinger login (Google SSO)" do?

Log into Hostinger via Google sign-in and land on hPanel, returning the signed-in account read back from Hostinger itself rather than echoed from the request. If the browser already has a Hostinger session it returns straight away. Asking for an account other than the live session is refused by name instead of attempted, because Hostinger will not show its sign-in form while any session is open — sign out of hPanel first to switch accounts. Needs the extension-paired browser, not a managed/cloud one.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to hostinger.com?

Yes. It acts as you on hostinger.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the hostinger.com cookies saved by the Reduck extension.

### Does it change anything on hostinger.com, or only read data?

It makes changes on hostinger.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hostinger.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hostinger.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/hostinger.com/login_with_google
