# Pipedrive whoami (signed-in account)

Report which Pipedrive account this browser is signed in as: the user id, email, name and company. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Pipedrive scripts.

- Site: pipedrive.com
- Address: `reduck/pipedrive.com/whoami`
- Updated: 2026-10-06 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pipedrive.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pipedrive.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `id` (string | null, optional)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `company` (string | null, optional): Pipedrive company subdomain (<company>.pipedrive.com).

## FAQ

### What does "Pipedrive whoami (signed-in account)" do?

Report which Pipedrive account this browser is signed in as: the user id, email, name and company. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Pipedrive scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, name, email, company, evidence, loggedIn.

### Do I need to be logged in to pipedrive.com?

Yes. It acts as you on pipedrive.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the pipedrive.com cookies saved by the Reduck extension.

### Does it change anything on pipedrive.com, or only read data?

It only reads. It looks things up on pipedrive.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pipedrive.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pipedrive.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pipedrive.com/whoami
