# Malt whoami (signed-in account)

Report which Malt account this browser is signed in as, if any: the account email. The browser does not need to be signed in: when it is signed out, the result is loggedIn false with no email, not an error. Use it to check the session before you run other Malt scripts.

- Site: malt.com
- Address: `reduck/malt.com/whoami`
- Updated: 2026-11-23 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/malt.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/malt.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `email` (string | null, optional)

## FAQ

### What does "Malt whoami (signed-in account)" do?

Report which Malt account this browser is signed in as, if any: the account email. The browser does not need to be signed in: when it is signed out, the result is loggedIn false with no email, not an error. Use it to check the session before you run other Malt scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, evidence, loggedIn.

### Do I need to be logged in to malt.com?

No. It only uses pages of malt.com that are reachable without signing in.

### Does it change anything on malt.com, or only read data?

It only reads. It looks things up on malt.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/malt.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/malt.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/malt.com/whoami
