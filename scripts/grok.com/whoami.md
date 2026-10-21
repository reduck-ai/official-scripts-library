# Grok whoami

Report which Grok account this browser is signed in as: the account email and name. When the browser is signed out of Grok, the run fails with a signed-out error asking you to sign in to grok.com.

- Site: grok.com
- Address: `reduck/grok.com/whoami`
- Updated: 2026-10-20 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/grok.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/grok.com/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Grok whoami" do?

Report which Grok account this browser is signed in as: the account email and name. When the browser is signed out of Grok, the run fails with a signed-out error asking you to sign in to grok.com.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, loggedIn.

### Do I need to be logged in to grok.com?

Yes. It acts as you on grok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the grok.com cookies saved by the Reduck extension.

### Does it change anything on grok.com, or only read data?

It only reads. It looks things up on grok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/grok.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/grok.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/grok.com/whoami
