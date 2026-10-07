# Substack whoami (signed-in account)

Report which Substack account this browser is signed in as: the @handle, display name, email and numeric user id. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Substack scripts.

- Site: substack.com
- Address: `reduck/substack.com/whoami`
- Updated: 2026-10-06 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/substack.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/substack.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `handle` (string | null, optional)
- `userId` (string | null, optional)

## FAQ

### What does "Substack whoami (signed-in account)" do?

Report which Substack account this browser is signed in as: the @handle, display name, email and numeric user id. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Substack scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, handle, userId, evidence, loggedIn.

### Do I need to be logged in to substack.com?

Yes. It acts as you on substack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the substack.com cookies saved by the Reduck extension.

### Does it change anything on substack.com, or only read data?

It only reads. It looks things up on substack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/substack.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/substack.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/substack.com/whoami
