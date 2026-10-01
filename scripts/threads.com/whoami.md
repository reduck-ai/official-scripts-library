# Threads whoami (signed-in account)

Report which Threads account this browser is signed in as: the user id and @username. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Threads scripts.

- Site: threads.com
- Address: `reduck/threads.com/whoami`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/threads.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/threads.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `id` (string | null, optional)
- `username` (string | null, optional)

## FAQ

### What does "Threads whoami (signed-in account)" do?

Report which Threads account this browser is signed in as: the user id and @username. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Threads scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, evidence, loggedIn, username.

### Do I need to be logged in to threads.com?

Yes. It acts as you on threads.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the threads.com cookies saved by the Reduck extension.

### Does it change anything on threads.com, or only read data?

It only reads. It looks things up on threads.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/threads.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/threads.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/threads.com/whoami
