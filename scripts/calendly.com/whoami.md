# Calendly whoami (signed-in account)

Report which Calendly account this browser is signed in as: the user id, email, name, timezone and organization id. Fails with a sign-in error when the browser is not signed in to Calendly.

- Site: calendly.com
- Address: `reduck/calendly.com/whoami`
- Updated: 2026-10-20 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendly.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendly.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `userId` (string | null, optional)
- `timezone` (string | null, optional)
- `organizationId` (string | null, optional)

## FAQ

### What does "Calendly whoami (signed-in account)" do?

Report which Calendly account this browser is signed in as: the user id, email, name, timezone and organization id. Fails with a sign-in error when the browser is not signed in to Calendly.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, userId, evidence, loggedIn, timezone, organizationId.

### Do I need to be logged in to calendly.com?

Yes. It acts as you on calendly.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendly.com cookies saved by the Reduck extension.

### Does it change anything on calendly.com, or only read data?

It only reads. It looks things up on calendly.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendly.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendly.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendly.com/whoami
