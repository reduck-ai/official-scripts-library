# 99designs whoami (signed-in account)

Report which 99designs account this browser is signed in as: the user id, display name, full name, whether it is a designer (and level), how it signs in (e.g. a Vista account) and which country site 99designs opened. 99designs does not render the account email. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other 99designs scripts.

- Site: 99designs.com
- Address: `reduck/99designs.com/whoami`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/99designs.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/99designs.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `site` (string | null, optional): The country site 99designs opened, e.g. 99designs.fr.
- `email` (string | null, optional)
- `userId` (string | null, optional)
- `fullName` (string | null, optional)
- `authMethod` (string | null, optional): How the account signs in, e.g. VISTAPRINT (Vista account).
- `isDesigner` (boolean | null, optional)
- `displayName` (string | null, optional)
- `designerLevel` (string | null, optional)

## FAQ

### What does "99designs whoami (signed-in account)" do?

Report which 99designs account this browser is signed in as: the user id, display name, full name, whether it is a designer (and level), how it signs in (e.g. a Vista account) and which country site 99designs opened. 99designs does not render the account email. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other 99designs scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns site, email, userId, evidence, fullName, loggedIn, authMethod, isDesigner, displayName, designerLevel.

### Do I need to be logged in to 99designs.com?

Yes. It acts as you on 99designs.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the 99designs.com cookies saved by the Reduck extension.

### Does it change anything on 99designs.com, or only read data?

It only reads. It looks things up on 99designs.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/99designs.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/99designs.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/99designs.com/whoami
