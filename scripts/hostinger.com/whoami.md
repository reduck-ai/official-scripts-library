# Hostinger whoami (signed-in account)

Report which Hostinger (hPanel) account this browser is signed in as: the account email. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Hostinger scripts.

- Site: hostinger.com
- Address: `reduck/hostinger.com/whoami`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hostinger.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hostinger.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `email` (string | null, optional)

## FAQ

### What does "Hostinger whoami (signed-in account)" do?

Report which Hostinger (hPanel) account this browser is signed in as: the account email. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Hostinger scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, evidence, loggedIn.

### Do I need to be logged in to hostinger.com?

Yes. It acts as you on hostinger.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the hostinger.com cookies saved by the Reduck extension.

### Does it change anything on hostinger.com, or only read data?

It only reads. It looks things up on hostinger.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hostinger.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hostinger.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/hostinger.com/whoami
