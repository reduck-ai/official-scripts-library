# HubSpot whoami (signed-in account)

Report which HubSpot account this browser is signed in as: the numeric user id, email, first name and last name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other HubSpot scripts.

- Site: app.hubspot.com
- Address: `reduck/app.hubspot.com/whoami`
- Updated: 2026-10-06 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.hubspot.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `email` (string | null, optional)
- `userId` (string | null, optional)
- `lastName` (string | null, optional)
- `firstName` (string | null, optional)

## FAQ

### What does "HubSpot whoami (signed-in account)" do?

Report which HubSpot account this browser is signed in as: the numeric user id, email, first name and last name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other HubSpot scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, userId, evidence, lastName, loggedIn, firstName.

### Do I need to be logged in to app.hubspot.com?

Yes. It acts as you on app.hubspot.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.hubspot.com cookies saved by the Reduck extension.

### Does it change anything on app.hubspot.com, or only read data?

It only reads. It looks things up on app.hubspot.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.hubspot.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.hubspot.com/whoami
