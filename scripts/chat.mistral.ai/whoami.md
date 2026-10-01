# Le Chat whoami (signed-in account)

Report which Mistral (Le Chat) account this browser is signed in as: email and name, from Mistral's own session service. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Le Chat scripts.

- Site: chat.mistral.ai
- Address: `reduck/chat.mistral.ai/whoami`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chat.mistral.ai/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)

## FAQ

### What does "Le Chat whoami (signed-in account)" do?

Report which Mistral (Le Chat) account this browser is signed in as: email and name, from Mistral's own session service. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Le Chat scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, loggedIn.

### Do I need to be logged in to chat.mistral.ai?

Yes. It acts as you on chat.mistral.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the chat.mistral.ai cookies saved by the Reduck extension.

### Does it change anything on chat.mistral.ai, or only read data?

It only reads. It looks things up on chat.mistral.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chat.mistral.ai/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chat.mistral.ai/whoami
