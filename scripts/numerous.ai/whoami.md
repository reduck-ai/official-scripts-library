# Numerous.ai whoami (signed-in account)

Report which Numerous.ai account this browser is signed in as: the user id, email and name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Numerous.ai scripts.

- Site: numerous.ai
- Address: `reduck/numerous.ai/whoami`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/numerous.ai/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/numerous.ai/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `email` (string | null, optional)

## FAQ

### What does "Numerous.ai whoami (signed-in account)" do?

Report which Numerous.ai account this browser is signed in as: the user id, email and name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Numerous.ai scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, evidence, loggedIn.

### Do I need to be logged in to numerous.ai?

Yes. It acts as you on numerous.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the numerous.ai cookies saved by the Reduck extension.

### Does it change anything on numerous.ai, or only read data?

It only reads. It looks things up on numerous.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/numerous.ai/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/numerous.ai/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/numerous.ai/whoami
