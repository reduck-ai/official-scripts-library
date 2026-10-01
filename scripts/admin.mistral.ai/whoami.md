# Mistral Admin whoami (signed-in account)

Report which Mistral account the Mistral admin console is signed in as in this browser: email and name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Mistral admin scripts.

- Site: admin.mistral.ai
- Address: `reduck/admin.mistral.ai/whoami`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.mistral.ai/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.mistral.ai/whoami
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

### What does "Mistral Admin whoami (signed-in account)" do?

Report which Mistral account the Mistral admin console is signed in as in this browser: email and name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Mistral admin scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, name, email, evidence, loggedIn.

### Do I need to be logged in to admin.mistral.ai?

Yes. It acts as you on admin.mistral.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.mistral.ai cookies saved by the Reduck extension.

### Does it change anything on admin.mistral.ai, or only read data?

It only reads. It looks things up on admin.mistral.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.mistral.ai/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.mistral.ai/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.mistral.ai/whoami
