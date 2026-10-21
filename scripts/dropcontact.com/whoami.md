# Dropcontact whoami (signed-in account)

Report which Dropcontact account this browser is signed in as: the account id and email. When the browser is signed out of Dropcontact, the run fails with a signed-out error that asks to sign in, so it can be used to check a session before running other Dropcontact scripts.

- Site: dropcontact.com
- Address: `reduck/dropcontact.com/whoami`
- Updated: 2026-10-20 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dropcontact.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dropcontact.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `id` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Dropcontact whoami (signed-in account)" do?

Report which Dropcontact account this browser is signed in as: the account id and email. When the browser is signed out of Dropcontact, the run fails with a signed-out error that asks to sign in, so it can be used to check a session before running other Dropcontact scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, email, evidence, loggedIn.

### Do I need to be logged in to dropcontact.com?

Yes. It acts as you on dropcontact.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dropcontact.com cookies saved by the Reduck extension.

### Does it change anything on dropcontact.com, or only read data?

It only reads. It looks things up on dropcontact.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dropcontact.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dropcontact.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dropcontact.com/whoami
