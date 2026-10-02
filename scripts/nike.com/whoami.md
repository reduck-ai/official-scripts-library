# Nike whoami (signed-in account)

Report which Nike Member account this browser is signed in as: the account email from Account settings. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Nike scripts.

- Site: nike.com
- Address: `reduck/nike.com/whoami`
- Updated: 2026-10-01 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/nike.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/nike.com/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `email` (string | null, optional)

## FAQ

### What does "Nike whoami (signed-in account)" do?

Report which Nike Member account this browser is signed in as: the account email from Account settings. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Nike scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, loggedIn.

### Do I need to be logged in to nike.com?

Yes. It acts as you on nike.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the nike.com cookies saved by the Reduck extension.

### Does it change anything on nike.com, or only read data?

It only reads. It looks things up on nike.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/nike.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nike.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/nike.com/whoami
