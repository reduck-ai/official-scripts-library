# Cursor whoami (signed-in account)

Report which Cursor account this browser is signed in as: the user id, email, name, plan (membership type) and team id. Being signed out, including an expired session, is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Cursor scripts.

- Site: cursor.com
- Address: `reduck/cursor.com/whoami`
- Updated: 2026-10-06 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cursor.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cursor.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `teamId` (number | null, optional)
- `userId` (string | null, optional)
- `membershipType` (string | null, optional)

## FAQ

### What does "Cursor whoami (signed-in account)" do?

Report which Cursor account this browser is signed in as: the user id, email, name, plan (membership type) and team id. Being signed out, including an expired session, is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Cursor scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, teamId, userId, evidence, loggedIn, membershipType.

### Do I need to be logged in to cursor.com?

Yes. It acts as you on cursor.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the cursor.com cookies saved by the Reduck extension.

### Does it change anything on cursor.com, or only read data?

It only reads. It looks things up on cursor.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cursor.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cursor.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cursor.com/whoami
