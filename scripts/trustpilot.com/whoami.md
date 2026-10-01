# Trustpilot whoami (signed-in account)

Report which Trustpilot account this browser is signed in as: email and display name from account settings. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Trustpilot scripts.

- Site: trustpilot.com
- Address: `reduck/trustpilot.com/whoami`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/trustpilot.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `email` (string | null, optional)
- `displayName` (string | null, optional)

## FAQ

### What does "Trustpilot whoami (signed-in account)" do?

Report which Trustpilot account this browser is signed in as: email and display name from account settings. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Trustpilot scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, loggedIn, displayName.

### Do I need to be logged in to trustpilot.com?

Yes. It acts as you on trustpilot.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the trustpilot.com cookies saved by the Reduck extension.

### Does it change anything on trustpilot.com, or only read data?

It only reads. It looks things up on trustpilot.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/trustpilot.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/trustpilot.com/whoami
