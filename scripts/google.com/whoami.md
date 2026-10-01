# Google whoami (signed-in account)

Report which Google account this browser is signed in as: display name and email, read from Google's account button on myaccount.google.com. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a Google session before running other Google scripts.

- Site: google.com
- Address: `reduck/google.com/whoami`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Google whoami (signed-in account)" do?

Report which Google account this browser is signed in as: display name and email, read from Google's account button on myaccount.google.com. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a Google session before running other Google scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, loggedIn.

### Do I need to be logged in to google.com?

Yes. It acts as you on google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the google.com cookies saved by the Reduck extension.

### Does it change anything on google.com, or only read data?

It only reads. It looks things up on google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/whoami
