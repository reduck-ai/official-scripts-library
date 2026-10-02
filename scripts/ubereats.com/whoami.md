# Uber Eats whoami (signed-in account)

Report which Uber Eats account this browser is signed in as: the account name, the email when Uber Eats exposes it, and a hashed email that identifies the account otherwise. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Uber Eats scripts.

- Site: ubereats.com
- Address: `reduck/ubereats.com/whoami`
- Updated: 2026-10-01 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ubereats.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ubereats.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional): Plain email, only when Uber Eats exposes it (usually null).
- `hashedEmail` (string | null, optional): SHA-256 of the lowercased account email, as Uber Eats reports it.

## FAQ

### What does "Uber Eats whoami (signed-in account)" do?

Report which Uber Eats account this browser is signed in as: the account name, the email when Uber Eats exposes it, and a hashed email that identifies the account otherwise. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Uber Eats scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, evidence, loggedIn, hashedEmail.

### Do I need to be logged in to ubereats.com?

Yes. It acts as you on ubereats.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the ubereats.com cookies saved by the Reduck extension.

### Does it change anything on ubereats.com, or only read data?

It only reads. It looks things up on ubereats.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ubereats.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ubereats.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ubereats.com/whoami
