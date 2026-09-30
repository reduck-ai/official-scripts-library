# Perplexity whoami

Report which Perplexity account this browser is signed in as: the account email and user id. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Perplexity scripts.

- Site: perplexity.ai
- Address: `reduck/perplexity.ai/whoami`
- Updated: 2026-09-29 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/perplexity.ai/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `email` (string | null, optional)
- `userId` (string | null, optional)

## FAQ

### What does "Perplexity whoami" do?

Report which Perplexity account this browser is signed in as: the account email and user id. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Perplexity scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, userId, loggedIn.

### Do I need to be logged in to perplexity.ai?

Yes. It acts as you on perplexity.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the perplexity.ai cookies saved by the Reduck extension.

### Does it change anything on perplexity.ai, or only read data?

It only reads. It looks things up on perplexity.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/perplexity.ai/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/perplexity.ai/whoami
