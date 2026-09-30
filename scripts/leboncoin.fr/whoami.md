# Leboncoin whoami

Report which Leboncoin account this browser is signed in as: the account email (and name when set), from Leboncoin's own account data. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Leboncoin scripts.

- Site: leboncoin.fr
- Address: `reduck/leboncoin.fr/whoami`
- Updated: 2026-09-29 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leboncoin.fr/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Leboncoin whoami" do?

Report which Leboncoin account this browser is signed in as: the account email (and name when set), from Leboncoin's own account data. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Leboncoin scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, loggedIn.

### Do I need to be logged in to leboncoin.fr?

Yes. It acts as you on leboncoin.fr: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the leboncoin.fr cookies saved by the Reduck extension.

### Does it change anything on leboncoin.fr, or only read data?

It only reads. It looks things up on leboncoin.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/leboncoin.fr/whoami
