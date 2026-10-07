# Gemini whoami (signed-in account)

Report which Google account this browser is signed in to Gemini as: the Google account id and email. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Gemini scripts.

- Site: gemini.google.com
- Address: `reduck/gemini.google.com/whoami`
- Updated: 2026-10-06 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gemini.google.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `email` (string | null, optional)
- `userId` (string | null, optional)

## FAQ

### What does "Gemini whoami (signed-in account)" do?

Report which Google account this browser is signed in to Gemini as: the Google account id and email. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Gemini scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, userId, evidence, loggedIn.

### Do I need to be logged in to gemini.google.com?

Yes. It acts as you on gemini.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the gemini.google.com cookies saved by the Reduck extension.

### Does it change anything on gemini.google.com, or only read data?

It only reads. It looks things up on gemini.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gemini.google.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/gemini.google.com/whoami
