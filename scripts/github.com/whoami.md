# GitHub whoami (signed-in account)

Report which GitHub account this browser is signed in as: the login (username), display name and avatar URL. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other GitHub scripts.

- Site: github.com
- Address: `reduck/github.com/whoami`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/github.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/github.com/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `login` (string | null, optional)
- `username` (string | null, optional)
- `avatarUrl` (string | null, optional)

## FAQ

### What does "GitHub whoami (signed-in account)" do?

Report which GitHub account this browser is signed in as: the login (username), display name and avatar URL. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other GitHub scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, login, loggedIn, username, avatarUrl.

### Do I need to be logged in to github.com?

Yes. It acts as you on github.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the github.com cookies saved by the Reduck extension.

### Does it change anything on github.com, or only read data?

It only reads. It looks things up on github.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/github.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/github.com/whoami
