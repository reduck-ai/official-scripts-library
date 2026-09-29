# Get current GitHub user

Automatically get current GitHub user on github.com. Report which GitHub account this browser is signed in as: the login, display name and avatar URL. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other GitHub scripts.

- Site: github.com
- Address: `reduck/github.com/get_current_user`
- Updated: 2026-09-28 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/github.com/get_current_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/github.com/get_current_user
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `login` (string | null, optional)
- `avatarUrl` (string | null, optional)

## FAQ

### What does "Get current GitHub user" do?

Report which GitHub account this browser is signed in as: the login, display name and avatar URL. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other GitHub scripts.

### How do I automatically get current GitHub user on github.com?

Ask an AI agent connected to Reduck to run reduck/github.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/get_current_user

### Is there a github.com API to get current GitHub user?

You do not need one. "Get current GitHub user" drives the real github.com pages in a browser, so it works whether or not github.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, login, loggedIn, avatarUrl.

### Do I need to be logged in to github.com?

Yes. It acts as you on github.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the github.com cookies saved by the Reduck extension.

### Does it change anything on github.com, or only read data?

It only reads. It looks things up on github.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/github.com/get_current_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/get_current_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/github.com/get_current_user
