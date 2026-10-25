# Instagram whoami (signed-in account)

Report which Instagram account this browser is signed in as: the user id, @username and name. When the browser is signed out of Instagram, the run fails with a signed-out error asking you to sign in to instagram.com.

- Site: instagram.com
- Address: `reduck/instagram.com/whoami`
- Updated: 2026-10-22 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `id` (string | null, optional)
- `name` (string | null, optional)
- `username` (string | null, optional)

## FAQ

### What does "Instagram whoami (signed-in account)" do?

Report which Instagram account this browser is signed in as: the user id, @username and name. When the browser is signed out of Instagram, the run fails with a signed-out error asking you to sign in to instagram.com.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns id, name, evidence, loggedIn, username.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/whoami
