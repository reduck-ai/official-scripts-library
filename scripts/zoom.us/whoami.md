# Zoom whoami (signed-in account)

Report which Zoom account this browser is signed in as: the user id, account id, sign-in email and the account's web domain (e.g. us05web.zoom.us). Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Zoom scripts. Works in any Zoom interface language.

- Site: zoom.us
- Address: `reduck/zoom.us/whoami`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/zoom.us/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/zoom.us/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `email` (string | null, optional)
- `userId` (string | null, optional)
- `accountId` (string | null, optional)
- `webDomain` (string | null, optional)

## FAQ

### What does "Zoom whoami (signed-in account)" do?

Report which Zoom account this browser is signed in as: the user id, account id, sign-in email and the account's web domain (e.g. us05web.zoom.us). Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Zoom scripts. Works in any Zoom interface language.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, userId, evidence, loggedIn, accountId, webDomain.

### Do I need to be logged in to zoom.us?

Yes. It acts as you on zoom.us: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the zoom.us cookies saved by the Reduck extension.

### Does it change anything on zoom.us, or only read data?

It only reads. It looks things up on zoom.us and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/zoom.us/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zoom.us/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/zoom.us/whoami
