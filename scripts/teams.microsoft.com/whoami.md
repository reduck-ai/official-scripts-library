# Teams whoami

Report which Microsoft Teams account this browser is signed in as — work or personal: email, name, whether it is a personal (consumer) or work account, and which Teams host it lives on (personal accounts are redirected to teams.live.com). Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session — and pick the right Teams host — before running other Teams scripts.

- Site: teams.microsoft.com
- Address: `reduck/teams.microsoft.com/whoami`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/teams.microsoft.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/teams.microsoft.com/whoami
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required)
- `host` (string | null, optional): The Teams host the account landed on
- `name` (string | null, optional)
- `email` (string | null, optional)
- `accountType` (string | null, optional): personal = consumer Microsoft account (Teams on teams.live.com); work = organization account

## FAQ

### What does "Teams whoami" do?

Report which Microsoft Teams account this browser is signed in as — work or personal: email, name, whether it is a personal (consumer) or work account, and which Teams host it lives on (personal accounts are redirected to teams.live.com). Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session — and pick the right Teams host — before running other Teams scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns host, name, email, loggedIn, accountType.

### Do I need to be logged in to teams.microsoft.com?

Yes. It acts as you on teams.microsoft.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the teams.microsoft.com cookies saved by the Reduck extension.

### Does it change anything on teams.microsoft.com, or only read data?

It only reads. It looks things up on teams.microsoft.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/teams.microsoft.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/teams.microsoft.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/teams.microsoft.com/whoami
