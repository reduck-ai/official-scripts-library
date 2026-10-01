# Google Docs whoami (signed-in account)

Report which Google account Google Docs/Sheets is signed in as in this browser: display name and email, read from Google's account button. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Docs or Sheets scripts.

- Site: docs.google.com
- Address: `reduck/docs.google.com/whoami`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Google Docs whoami (signed-in account)" do?

Report which Google account Google Docs/Sheets is signed in as in this browser: display name and email, read from Google's account button. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Docs or Sheets scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, loggedIn.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It only reads. It looks things up on docs.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/whoami
