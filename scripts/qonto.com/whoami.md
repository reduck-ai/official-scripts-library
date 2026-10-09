# Qonto whoami (signed-in account)

Report which Qonto account this browser is signed in as: the account email. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Qonto scripts.

- Site: qonto.com
- Address: `reduck/qonto.com/whoami`
- Updated: 2026-10-08 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/qonto.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/qonto.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `email` (string | null, optional)

## FAQ

### What does "Qonto whoami (signed-in account)" do?

Report which Qonto account this browser is signed in as: the account email. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Qonto scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, evidence, loggedIn.

### Do I need to be logged in to qonto.com?

Yes. It acts as you on qonto.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the qonto.com cookies saved by the Reduck extension.

### Does it change anything on qonto.com, or only read data?

It only reads. It looks things up on qonto.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/qonto.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/qonto.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/qonto.com/whoami
