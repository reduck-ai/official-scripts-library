# Trello whoami (signed-in account)

Report which Trello account this browser is signed in as: the member id, username, full name and email. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Trello scripts.

- Site: trello.com
- Address: `reduck/trello.com/whoami`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/trello.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/trello.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `id` (string | null, optional)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `username` (string | null, optional)

## FAQ

### What does "Trello whoami (signed-in account)" do?

Report which Trello account this browser is signed in as: the member id, username, full name and email. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Trello scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, name, email, evidence, loggedIn, username.

### Do I need to be logged in to trello.com?

Yes. It acts as you on trello.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the trello.com cookies saved by the Reduck extension.

### Does it change anything on trello.com, or only read data?

It only reads. It looks things up on trello.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/trello.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trello.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/trello.com/whoami
