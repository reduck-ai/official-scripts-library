# Noota whoami

Report which Noota account this browser is signed in as: the account email (and name when set), from Noota's own users/me. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Noota scripts.

- Site: noota.io
- Address: `reduck/noota.io/whoami`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/noota.io/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/noota.io/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Noota whoami" do?

Report which Noota account this browser is signed in as: the account email (and name when set), from Noota's own users/me. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Noota scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, loggedIn.

### Do I need to be logged in to noota.io?

Yes. It acts as you on noota.io: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the noota.io cookies saved by the Reduck extension.

### Does it change anything on noota.io, or only read data?

It only reads. It looks things up on noota.io and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/noota.io/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/noota.io/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/noota.io/whoami
