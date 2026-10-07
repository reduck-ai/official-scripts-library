# Browserbase whoami (signed-in account)

Report which Browserbase account this browser is signed in as: the user id, email, name, account creation date, and every organization it belongs to with its slug (the org other Browserbase scripts take) and role. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Browserbase scripts.

- Site: browserbase.com
- Address: `reduck/browserbase.com/whoami`
- Updated: 2026-10-06 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/browserbase.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/browserbase.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `userId` (string | null, optional)
- `createdAt` (string | null, optional)
- `organizations` (array, optional)

## FAQ

### What does "Browserbase whoami (signed-in account)" do?

Report which Browserbase account this browser is signed in as: the user id, email, name, account creation date, and every organization it belongs to with its slug (the org other Browserbase scripts take) and role. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Browserbase scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, userId, evidence, loggedIn, createdAt, organizations.

### Do I need to be logged in to browserbase.com?

Yes. It acts as you on browserbase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the browserbase.com cookies saved by the Reduck extension.

### Does it change anything on browserbase.com, or only read data?

It only reads. It looks things up on browserbase.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/browserbase.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/browserbase.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/browserbase.com/whoami
