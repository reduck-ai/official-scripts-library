# Luma whoami (signed-in account)

Report which Luma account this browser is signed in as: the user id, username, display name and email. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Luma scripts.

- Site: luma.com
- Address: `reduck/luma.com/whoami`
- Updated: 2026-09-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/luma.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/luma.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `userId` (string | null, optional): Luma user id, e.g. usr-XXXXXXXXXXXXXXX.
- `username` (string | null, optional): Luma username (luma.com/user/<username>); null when the account never picked one.

## FAQ

### What does "Luma whoami (signed-in account)" do?

Report which Luma account this browser is signed in as: the user id, username, display name and email. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Luma scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, userId, evidence, loggedIn, username.

### Do I need to be logged in to luma.com?

Yes. It acts as you on luma.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the luma.com cookies saved by the Reduck extension.

### Does it change anything on luma.com, or only read data?

It only reads. It looks things up on luma.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/luma.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/luma.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/luma.com/whoami
