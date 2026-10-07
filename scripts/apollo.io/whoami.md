# Apollo whoami

Report which Apollo account this browser is signed in as: email and name, from the app's own session check. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Apollo scripts.

- Site: apollo.io
- Address: `reduck/apollo.io/whoami`
- Updated: 2026-10-06 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/apollo.io/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/apollo.io/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Apollo whoami" do?

Report which Apollo account this browser is signed in as: email and name, from the app's own session check. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Apollo scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, loggedIn.

### Do I need to be logged in to apollo.io?

Yes. It acts as you on apollo.io: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the apollo.io cookies saved by the Reduck extension.

### Does it change anything on apollo.io, or only read data?

It only reads. It looks things up on apollo.io and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/apollo.io/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/apollo.io/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/apollo.io/whoami
