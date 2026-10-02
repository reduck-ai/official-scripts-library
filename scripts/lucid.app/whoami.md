# Lucid whoami (signed-in account)

Report which Lucid (Lucidchart / Lucidspark) account this browser is signed in as: the user id, email and name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Lucid scripts.

- Site: lucid.app
- Address: `reduck/lucid.app/whoami`
- Updated: 2026-10-01 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lucid.app/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lucid.app/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `id` (string | null, optional)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Lucid whoami (signed-in account)" do?

Report which Lucid (Lucidchart / Lucidspark) account this browser is signed in as: the user id, email and name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Lucid scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, name, email, evidence, loggedIn.

### Do I need to be logged in to lucid.app?

Yes. It acts as you on lucid.app: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the lucid.app cookies saved by the Reduck extension.

### Does it change anything on lucid.app, or only read data?

It only reads. It looks things up on lucid.app and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lucid.app/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lucid.app/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/lucid.app/whoami
