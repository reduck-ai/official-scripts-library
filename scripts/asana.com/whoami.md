# Asana whoami (signed-in account)

Report which Asana account this browser is signed in as: name, email and user gid, from Asana's own users/me. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Asana scripts.

- Site: asana.com
- Address: `reduck/asana.com/whoami`
- Updated: 2026-10-01 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/asana.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/asana.com/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `gid` (string | null, optional)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Asana whoami (signed-in account)" do?

Report which Asana account this browser is signed in as: name, email and user gid, from Asana's own users/me. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Asana scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns gid, name, email, loggedIn.

### Do I need to be logged in to asana.com?

Yes. It acts as you on asana.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the asana.com cookies saved by the Reduck extension.

### Does it change anything on asana.com, or only read data?

It only reads. It looks things up on asana.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/asana.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/asana.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/asana.com/whoami
