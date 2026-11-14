# Dealroom whoami

Report which Dealroom account this browser is signed in as: email, name and user id, from the dashboard's own page data. A signed-out browser is reported as not logged in, so it can be used to check a session before running other Dealroom scripts.

- Site: dealroom.co
- Address: `reduck/dealroom.co/whoami`
- Updated: 2026-11-13 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dealroom.co/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dealroom.co/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `id` (string | null, optional): Dealroom user id
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Dealroom whoami" do?

Report which Dealroom account this browser is signed in as: email, name and user id, from the dashboard's own page data. A signed-out browser is reported as not logged in, so it can be used to check a session before running other Dealroom scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, name, email, loggedIn.

### Do I need to be logged in to dealroom.co?

Yes. It acts as you on dealroom.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dealroom.co cookies saved by the Reduck extension.

### Does it change anything on dealroom.co, or only read data?

It only reads. It looks things up on dealroom.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dealroom.co/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dealroom.co/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dealroom.co/whoami
