# Make whoami (signed-in account)

Report which Make (make.com) account this browser is signed in as: the user id, email and name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Make scripts.

- Site: make.com
- Address: `reduck/make.com/whoami`
- Updated: 2026-10-06 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/make.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/make.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `id` (string | null, optional)
- `name` (string | null, optional)
- `zone` (string | null, optional): Make zone host the account lives on, e.g. eu1.make.com.
- `email` (string | null, optional)

## FAQ

### What does "Make whoami (signed-in account)" do?

Report which Make (make.com) account this browser is signed in as: the user id, email and name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Make scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, name, zone, email, evidence, loggedIn.

### Do I need to be logged in to make.com?

Yes. It acts as you on make.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the make.com cookies saved by the Reduck extension.

### Does it change anything on make.com, or only read data?

It only reads. It looks things up on make.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/make.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/make.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/make.com/whoami
