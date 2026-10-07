# Pulley whoami (signed-in account)

Report which Pulley account this browser is signed in as: the user id, email, name, whether two-factor auth is on, when the account was created, the companies it belongs to, and on how many cap tables it holds equity. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Pulley scripts.

- Site: pulley.com
- Address: `reduck/pulley.com/whoami`
- Updated: 2026-10-06 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pulley.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pulley.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `has2fa` (boolean | null, optional)
- `userId` (string | null, optional)
- `companies` (array, optional): Companies (Pulley firms) the user belongs to, as Pulley returns them.
- `createdAt` (string | null, optional)
- `stakeholderCount` (integer | null, optional): How many cap tables the user holds equity on as a stakeholder.

## FAQ

### What does "Pulley whoami (signed-in account)" do?

Report which Pulley account this browser is signed in as: the user id, email, name, whether two-factor auth is on, when the account was created, the companies it belongs to, and on how many cap tables it holds equity. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Pulley scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, has2fa, userId, evidence, loggedIn, companies, createdAt, stakeholderCount.

### Do I need to be logged in to pulley.com?

Yes. It acts as you on pulley.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the pulley.com cookies saved by the Reduck extension.

### Does it change anything on pulley.com, or only read data?

It only reads. It looks things up on pulley.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pulley.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pulley.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pulley.com/whoami
