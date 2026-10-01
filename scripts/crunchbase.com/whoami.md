# Crunchbase whoami (signed-in account)

Report which Crunchbase account this browser is signed in as: email, first name and last name from Account Settings > Your Info. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Crunchbase scripts.

- Site: crunchbase.com
- Address: `reduck/crunchbase.com/whoami`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crunchbase.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `email` (string | null, optional)
- `lastName` (string | null, optional)
- `firstName` (string | null, optional)

## FAQ

### What does "Crunchbase whoami (signed-in account)" do?

Report which Crunchbase account this browser is signed in as: email, first name and last name from Account Settings > Your Info. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Crunchbase scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, lastName, loggedIn, firstName.

### Do I need to be logged in to crunchbase.com?

Yes. It acts as you on crunchbase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the crunchbase.com cookies saved by the Reduck extension.

### Does it change anything on crunchbase.com, or only read data?

It only reads. It looks things up on crunchbase.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/crunchbase.com/whoami
