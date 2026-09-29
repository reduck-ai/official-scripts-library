# ngrok whoami (signed-in account)

Report which ngrok dashboard account this browser is signed in as: the email, numeric account id and plan (Free, Personal, Pro…). Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other ngrok scripts.

- Site: dashboard.ngrok.com
- Address: `reduck/dashboard.ngrok.com/whoami`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dashboard.ngrok.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dashboard.ngrok.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `plan` (string | null, optional)
- `email` (string | null, optional)
- `accountId` (string | null, optional)

## FAQ

### What does "ngrok whoami (signed-in account)" do?

Report which ngrok dashboard account this browser is signed in as: the email, numeric account id and plan (Free, Personal, Pro…). Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other ngrok scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns plan, email, evidence, loggedIn, accountId.

### Do I need to be logged in to dashboard.ngrok.com?

Yes. It acts as you on dashboard.ngrok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dashboard.ngrok.com cookies saved by the Reduck extension.

### Does it change anything on dashboard.ngrok.com, or only read data?

It only reads. It looks things up on dashboard.ngrok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dashboard.ngrok.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dashboard.ngrok.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dashboard.ngrok.com/whoami
