# Canva login

Log into Canva via Google SSO and land in the Canva app, returning the signed-in account read back out of the app itself. If the browser already has a Canva session it returns straight away without touching canva.com/login (that page closes its own tab a few seconds after load whenever a session exists). Asking for an account other than the live session is refused by name rather than attempted, because Canva will not show its sign-in modal while any session is open. Needs the extension-paired browser, not a managed/cloud one.

- Site: canva.com
- Address: `reduck/canva.com/login_with_google`
- Updated: 2026-08-24 (v14)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/canva.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/canva.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the existing Canva session, or the first/only Google account when signed out.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional): The signed-in Canva account, read back from the app document (Canva embeds the session email in the /projects shell) — never an unverified echo of the `email` argument. Null only when no address could be read.

## FAQ

### What does "Canva login" do?

Log into Canva via Google SSO and land in the Canva app, returning the signed-in account read back out of the app itself. If the browser already has a Canva session it returns straight away without touching canva.com/login (that page closes its own tab a few seconds after load whenever a session exists). Asking for an account other than the live session is refused by name rather than attempted, because Canva will not show its sign-in modal while any session is open. Needs the extension-paired browser, not a managed/cloud one.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to canva.com?

Yes. It acts as you on canva.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the canva.com cookies saved by the Reduck extension.

### Does it change anything on canva.com, or only read data?

It makes changes on canva.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/canva.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/canva.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/canva.com/login_with_google
