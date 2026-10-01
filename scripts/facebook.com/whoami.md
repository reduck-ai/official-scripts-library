# Facebook whoami (signed-in account)

Report which Facebook account this browser is signed in as: the user id and name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Facebook scripts. It never signs in.

- Site: facebook.com
- Address: `reduck/facebook.com/whoami`
- Updated: 2026-09-30 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `id` (string | null, optional)
- `name` (string | null, optional)

## FAQ

### What does "Facebook whoami (signed-in account)" do?

Report which Facebook account this browser is signed in as: the user id and name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Facebook scripts. It never signs in.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, name, evidence, loggedIn.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/whoami
