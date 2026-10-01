# Dust whoami (signed-in account)

Report which Dust account this browser is signed in as: the user id, email and name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Dust scripts.

- Site: dust.tt
- Address: `reduck/dust.tt/whoami`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dust.tt/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dust.tt/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `id` (string | null, optional): Dust user sId.
- `name` (string | null, optional)
- `email` (string | null, optional)
- `username` (string | null, optional)

## FAQ

### What does "Dust whoami (signed-in account)" do?

Report which Dust account this browser is signed in as: the user id, email and name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Dust scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, name, email, evidence, loggedIn, username.

### Do I need to be logged in to dust.tt?

Yes. It acts as you on dust.tt: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dust.tt cookies saved by the Reduck extension.

### Does it change anything on dust.tt, or only read data?

It only reads. It looks things up on dust.tt and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dust.tt/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dust.tt/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dust.tt/whoami
