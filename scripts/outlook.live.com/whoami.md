# Outlook whoami (signed-in Microsoft account)

Report which Microsoft account this browser is signed in to Outlook.com with: the email address and display name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Outlook scripts.

- Site: outlook.live.com
- Address: `reduck/outlook.live.com/whoami`
- Updated: 2026-09-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/outlook.live.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Outlook whoami (signed-in Microsoft account)" do?

Report which Microsoft account this browser is signed in to Outlook.com with: the email address and display name. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Outlook scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, evidence, loggedIn.

### Do I need to be logged in to outlook.live.com?

Yes. It acts as you on outlook.live.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the outlook.live.com cookies saved by the Reduck extension.

### Does it change anything on outlook.live.com, or only read data?

It only reads. It looks things up on outlook.live.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/outlook.live.com/whoami
