# Lovable login (Google SSO)

Sign in to Lovable with Google and land on the dashboard, ready for the scripts that need a signed-in session. Already signed in, it returns straight away instead of repeating the sign-in. Works whatever language Lovable is displayed in.

- Site: lovable.dev
- Address: `reduck/lovable.dev/login_with_google`
- Updated: 2026-08-21 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lovable.dev/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lovable.dev/login_with_google
```

## Input

- `email` (string, optional): Google account to pick if Google shows an account chooser. Omit to use the single signed-in account.

## Output

- `url` (string, required): The Lovable URL the run landed on once signed in.
- `loggedIn` (boolean, required)
- `account` (string | null, optional): Echo of the email argument — which Google account the run was told to pick. Null when the caller did not specify one. This is the request, not verified session evidence: Lovable surfaces no account email on the signed-in page, so there is nothing to read it back from.

## FAQ

### What does "Lovable login (Google SSO)" do?

Sign in to Lovable with Google and land on the dashboard, ready for the scripts that need a signed-in session. Already signed in, it returns straight away instead of repeating the sign-in. Works whatever language Lovable is displayed in.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to lovable.dev?

Yes. It acts as you on lovable.dev: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the lovable.dev cookies saved by the Reduck extension.

### Does it change anything on lovable.dev, or only read data?

It makes changes on lovable.dev, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lovable.dev/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lovable.dev/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/lovable.dev/login_with_google
