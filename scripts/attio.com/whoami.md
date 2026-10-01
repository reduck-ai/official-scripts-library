# Attio whoami (signed-in account)

Report which Attio account this browser is signed in as: the user id, email and name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Attio scripts.

- Site: attio.com
- Address: `reduck/attio.com/whoami`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/attio.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/attio.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `id` (string | null, optional)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `workspace` (string | null, optional): Slug of the workspace the app opened (app.attio.com/<workspace>).

## FAQ

### What does "Attio whoami (signed-in account)" do?

Report which Attio account this browser is signed in as: the user id, email and name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Attio scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, name, email, evidence, loggedIn, workspace.

### Do I need to be logged in to attio.com?

Yes. It acts as you on attio.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the attio.com cookies saved by the Reduck extension.

### Does it change anything on attio.com, or only read data?

It only reads. It looks things up on attio.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/attio.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/attio.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/attio.com/whoami
