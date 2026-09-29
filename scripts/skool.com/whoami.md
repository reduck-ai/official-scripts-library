# Skool whoami

Report which Skool account this browser is signed in as: email, name and profile handle, from the settings page's own data. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Skool scripts.

- Site: skool.com
- Address: `reduck/skool.com/whoami`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/skool.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/skool.com/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `handle` (string | null, optional): Skool profile handle, e.g. vincent-lambert-8912

## FAQ

### What does "Skool whoami" do?

Report which Skool account this browser is signed in as: email, name and profile handle, from the settings page's own data. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Skool scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, handle, loggedIn.

### Do I need to be logged in to skool.com?

Yes. It acts as you on skool.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the skool.com cookies saved by the Reduck extension.

### Does it change anything on skool.com, or only read data?

It only reads. It looks things up on skool.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/skool.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/skool.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/skool.com/whoami
