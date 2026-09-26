# Discord whoami (signed-in account)

Report which Discord account this browser is signed in as: the username, display name, email and user id. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Discord scripts.

- Site: discord.com
- Address: `reduck/discord.com/whoami`
- Updated: 2026-09-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `email` (string | null, optional)
- `userId` (string | null, optional)
- `username` (string | null, optional)
- `displayName` (string | null, optional)

## FAQ

### What does "Discord whoami (signed-in account)" do?

Report which Discord account this browser is signed in as: the username, display name, email and user id. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Discord scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns email, userId, evidence, loggedIn, username, displayName.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It only reads. It looks things up on discord.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/whoami
