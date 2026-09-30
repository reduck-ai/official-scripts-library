# Claude Console login (Google SSO)

Log into the Claude Console (platform.claude.com, formerly console.anthropic.com) with Continue with Google. Returns straight away if you are already signed in, and reports the account.

- Site: console.anthropic.com
- Address: `reduck/console.anthropic.com/login_with_google`
- Updated: 2026-09-29 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.anthropic.com/login_with_google`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.anthropic.com/login_with_google
```

## Input

- `email` (string, optional): Google account to pick in the chooser. Omit to use the first account listed.

## Output

- `url` (string, required)
- `already` (boolean, required): true when a session already existed and no sign-in was needed
- `loggedIn` (boolean, required)
- `name` (string | null, optional): Console display name
- `account` (string | null, optional): Console account email

## FAQ

### What does "Claude Console login (Google SSO)" do?

Log into the Claude Console (platform.claude.com, formerly console.anthropic.com) with Continue with Google. Returns straight away if you are already signed in, and reports the account.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns url, name, account, already, loggedIn.

### Do I need to be logged in to console.anthropic.com?

No. It only uses pages of console.anthropic.com that are reachable without signing in.

### Does it change anything on console.anthropic.com, or only read data?

It makes changes on console.anthropic.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.anthropic.com/login_with_google, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.anthropic.com/login_with_google

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/console.anthropic.com/login_with_google
