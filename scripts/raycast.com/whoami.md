# Raycast whoami (signed-in account)

Report which Raycast account this browser is signed in as: the user id, Raycast handle, name, email and whether it has Pro features. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Raycast scripts.

- Site: raycast.com
- Address: `reduck/raycast.com/whoami`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/raycast.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/raycast.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `handle` (string | null, optional): The account's Raycast handle (raycast.com/<handle>).
- `hasPro` (boolean | null, optional)
- `userId` (string | null, optional)

## FAQ

### What does "Raycast whoami (signed-in account)" do?

Report which Raycast account this browser is signed in as: the user id, Raycast handle, name, email and whether it has Pro features. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Raycast scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, handle, hasPro, userId, evidence, loggedIn.

### Do I need to be logged in to raycast.com?

Yes. It acts as you on raycast.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the raycast.com cookies saved by the Reduck extension.

### Does it change anything on raycast.com, or only read data?

It only reads. It looks things up on raycast.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/raycast.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/raycast.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/raycast.com/whoami
