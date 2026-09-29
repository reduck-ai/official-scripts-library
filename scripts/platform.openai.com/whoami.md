# OpenAI Platform whoami

Report which OpenAI API Platform account this browser is signed in as: the account email, name and default organization. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other platform.openai.com scripts.

- Site: platform.openai.com
- Address: `reduck/platform.openai.com/whoami`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/platform.openai.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/platform.openai.com/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `email` (string | null, optional)
- `organization` (string | null, optional)

## FAQ

### What does "OpenAI Platform whoami" do?

Report which OpenAI API Platform account this browser is signed in as: the account email, name and default organization. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other platform.openai.com scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, email, loggedIn, organization.

### Do I need to be logged in to platform.openai.com?

Yes. It acts as you on platform.openai.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the platform.openai.com cookies saved by the Reduck extension.

### Does it change anything on platform.openai.com, or only read data?

It only reads. It looks things up on platform.openai.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/platform.openai.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/platform.openai.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/platform.openai.com/whoami
