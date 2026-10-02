# Neon console whoami (signed-in account)

Report which Neon console account this browser is signed in as: email, first name and last name from Account settings > Profile. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Neon console scripts.

- Site: console.neon.tech
- Address: `reduck/console.neon.tech/whoami`
- Updated: 2026-10-01 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.neon.tech/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `email` (string | null, optional)
- `lastName` (string | null, optional)
- `firstName` (string | null, optional)

## FAQ

### What does "Neon console whoami (signed-in account)" do?

Report which Neon console account this browser is signed in as: email, first name and last name from Account settings > Profile. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Neon console scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, lastName, loggedIn, firstName.

### Do I need to be logged in to console.neon.tech?

Yes. It acts as you on console.neon.tech: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the console.neon.tech cookies saved by the Reduck extension.

### Does it change anything on console.neon.tech, or only read data?

It only reads. It looks things up on console.neon.tech and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.neon.tech/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/console.neon.tech/whoami
