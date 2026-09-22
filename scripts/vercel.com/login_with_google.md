# Vercel login (Google SSO)

Log into Vercel using Sign in with Google, ending on your Vercel dashboard. Returns straight away if you are already signed in, so it is safe to run repeatedly. Optionally pass which Google account to pick when several are signed in.

- Site: vercel.com
- Address: `reduck/vercel.com/login_with_google`
- Updated: 2026-08-21 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/vercel.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/vercel.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick if the chooser appears. Omit to use the first/only account.

## Output

- `url` (string, required)
- `loggedIn` (boolean, required)
- `account` (string | null, optional): The signed-in Vercel account, read back from Vercel's own session endpoint. Null when no email could be read — never an unverified echo of the `email` argument.

## FAQ

### What does "Vercel login (Google SSO)" do?

Log into Vercel using Sign in with Google, ending on your Vercel dashboard. Returns straight away if you are already signed in, so it is safe to run repeatedly. Optionally pass which Google account to pick when several are signed in.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, account, loggedIn.

### Do I need to be logged in to vercel.com?

Yes. It acts as you on vercel.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the vercel.com cookies saved by the Reduck extension.

### Does it change anything on vercel.com, or only read data?

It makes changes on vercel.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/vercel.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vercel.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/vercel.com/login_with_google
