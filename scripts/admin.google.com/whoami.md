# Google Admin whoami (signed-in account)

Report which Google account the Google Admin console is signed in as in this browser: display name and email. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Google Admin scripts.

- Site: admin.google.com
- Address: `reduck/admin.google.com/whoami`
- Updated: 2026-10-01 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.google.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.google.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Google Admin whoami (signed-in account)" do?

Report which Google account the Google Admin console is signed in as in this browser: display name and email. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Google Admin scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, evidence, loggedIn.

### Do I need to be logged in to admin.google.com?

Yes. It acts as you on admin.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.google.com cookies saved by the Reduck extension.

### Does it change anything on admin.google.com, or only read data?

It only reads. It looks things up on admin.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.google.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.google.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.google.com/whoami
