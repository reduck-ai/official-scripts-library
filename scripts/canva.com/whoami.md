# Canva whoami (signed-in account)

Report which Canva account this browser is signed in as: the user id, email, display name and username. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Canva scripts.

- Site: canva.com
- Address: `reduck/canva.com/whoami`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/canva.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/canva.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `email` (string | null, optional)
- `userId` (string | null, optional)
- `username` (string | null, optional)
- `displayName` (string | null, optional)

## FAQ

### What does "Canva whoami (signed-in account)" do?

Report which Canva account this browser is signed in as: the user id, email, display name and username. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Canva scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, userId, evidence, loggedIn, username, displayName.

### Do I need to be logged in to canva.com?

Yes. It acts as you on canva.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the canva.com cookies saved by the Reduck extension.

### Does it change anything on canva.com, or only read data?

It only reads. It looks things up on canva.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/canva.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/canva.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/canva.com/whoami
