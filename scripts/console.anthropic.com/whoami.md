# Anthropic Console whoami (signed-in account)

Report which Anthropic Console (platform.claude.com) account this browser is signed in as: the user id, uuid, email, name, and every organization it belongs to with its uuid and role (the organization other Console scripts act on). Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Console scripts.

- Site: console.anthropic.com
- Address: `reduck/console.anthropic.com/whoami`
- Updated: 2026-10-06 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.anthropic.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.anthropic.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `uuid` (string | null, optional)
- `email` (string | null, optional)
- `userId` (string | null, optional)
- `organizations` (array, optional)

## FAQ

### What does "Anthropic Console whoami (signed-in account)" do?

Report which Anthropic Console (platform.claude.com) account this browser is signed in as: the user id, uuid, email, name, and every organization it belongs to with its uuid and role (the organization other Console scripts act on). Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Console scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, uuid, email, userId, evidence, loggedIn, organizations.

### Do I need to be logged in to console.anthropic.com?

Yes. It acts as you on console.anthropic.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the console.anthropic.com cookies saved by the Reduck extension.

### Does it change anything on console.anthropic.com, or only read data?

It only reads. It looks things up on console.anthropic.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.anthropic.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.anthropic.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/console.anthropic.com/whoami
