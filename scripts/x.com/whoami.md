# X (Twitter) whoami (signed-in account)

Report which X (Twitter) account this browser is signed in as: the @handle, display name and numeric user id. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other X scripts.

- Site: x.com
- Address: `reduck/x.com/whoami`
- Updated: 2026-09-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `handle` (string | null, optional)
- `userId` (string | null, optional)

## FAQ

### What does "X (Twitter) whoami (signed-in account)" do?

Report which X (Twitter) account this browser is signed in as: the @handle, display name and numeric user id. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other X scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, handle, userId, evidence, loggedIn.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/whoami
