# Drata whoami (signed-in account)

Report which Drata account this browser is signed in as: the user id, email, first and last name, roles, account type, and the workspace and region the app opened. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Drata scripts.

- Site: drata.com
- Address: `reduck/drata.com/whoami`
- Updated: 2026-09-29 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drata.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drata.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `email` (string | null, optional)
- `roles` (array, optional)
- `region` (string | null, optional)
- `userId` (string | null, optional)
- `lastName` (string | null, optional)
- `firstName` (string | null, optional)
- `accountType` (string | null, optional)
- `workspaceSlug` (string | null, optional)

## FAQ

### What does "Drata whoami (signed-in account)" do?

Report which Drata account this browser is signed in as: the user id, email, first and last name, roles, account type, and the workspace and region the app opened. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Drata scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, roles, region, userId, evidence, lastName, loggedIn, firstName, accountType, workspaceSlug.

### Do I need to be logged in to drata.com?

Yes. It acts as you on drata.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drata.com cookies saved by the Reduck extension.

### Does it change anything on drata.com, or only read data?

It only reads. It looks things up on drata.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drata.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drata.com/whoami
