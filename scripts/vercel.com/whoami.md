# Vercel whoami (signed-in account)

Report which Vercel account this browser is signed in as: the user id, email, username, plan, default team and every team it belongs to with its role (the team slug other Vercel scripts take). Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Vercel scripts.

- Site: vercel.com
- Address: `reduck/vercel.com/whoami`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/vercel.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/vercel.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `plan` (string | null, optional)
- `email` (string | null, optional)
- `teams` (array, optional)
- `userId` (string | null, optional)
- `username` (string | null, optional)
- `defaultTeamId` (string | null, optional)

## FAQ

### What does "Vercel whoami (signed-in account)" do?

Report which Vercel account this browser is signed in as: the user id, email, username, plan, default team and every team it belongs to with its role (the team slug other Vercel scripts take). Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Vercel scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, plan, email, teams, userId, evidence, loggedIn, username, defaultTeamId.

### Do I need to be logged in to vercel.com?

Yes. It acts as you on vercel.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the vercel.com cookies saved by the Reduck extension.

### Does it change anything on vercel.com, or only read data?

It only reads. It looks things up on vercel.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/vercel.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vercel.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/vercel.com/whoami
