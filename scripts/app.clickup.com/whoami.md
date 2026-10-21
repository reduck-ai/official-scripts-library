# ClickUp whoami (signed-in account)

Report which ClickUp account this browser is signed in as: full name and email. Fails with a sign-in error when the browser is not signed in to ClickUp.

- Site: app.clickup.com
- Address: `reduck/app.clickup.com/whoami`
- Updated: 2026-10-20 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.clickup.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "ClickUp whoami (signed-in account)" do?

Report which ClickUp account this browser is signed in as: full name and email. Fails with a sign-in error when the browser is not signed in to ClickUp.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, evidence, loggedIn.

### Do I need to be logged in to app.clickup.com?

Yes. It acts as you on app.clickup.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.clickup.com cookies saved by the Reduck extension.

### Does it change anything on app.clickup.com, or only read data?

It only reads. It looks things up on app.clickup.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.clickup.com/whoami
