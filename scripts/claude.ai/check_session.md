# Check Claude.ai session

Automatically check Claude.ai session on claude.ai. Report whether the browser is signed in to Claude.ai, and as which account. Returns connected (true or false) and account (the sign-in email, or null when signed out). A signed-out browser is a normal answer, not an error, so this can be used as the session check that runs before another Claude.ai script.

- Site: claude.ai
- Address: `reduck/claude.ai/check_session`
- Updated: 2026-11-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/check_session`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/check_session
```

## Input

It takes no input.

## Output

- `account` (string | null, required): The sign-in email of that session, or null when signed out.
- `connected` (boolean, required): True when the browser holds a live Claude.ai session.

## FAQ

### What does "Check Claude.ai session" do?

Report whether the browser is signed in to Claude.ai, and as which account. Returns connected (true or false) and account (the sign-in email, or null when signed out). A signed-out browser is a normal answer, not an error, so this can be used as the session check that runs before another Claude.ai script.

### How do I automatically check Claude.ai session on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/check_session, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/check_session

### Is there a claude.ai API to check Claude.ai session?

You do not need one. "Check Claude.ai session" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns account, connected.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It only reads. It looks things up on claude.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/check_session, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/check_session

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/check_session
