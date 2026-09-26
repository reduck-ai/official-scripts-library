# Slack whoami (signed-in account)

Report which Slack account this browser is signed in as: the user's name, email, user id and the active workspace. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Slack scripts.

- Site: slack.com
- Address: `reduck/slack.com/whoami`
- Updated: 2026-09-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/whoami`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/whoami
```

## Input

It takes no input.

## Output

- `evidence` (string, required)
- `loggedIn` (boolean, required)
- `name` (string | null, optional)
- `team` (string | null, optional)
- `email` (string | null, optional)
- `teamId` (string | null, optional)
- `userId` (string | null, optional)
- `teamUrl` (string | null, optional)

## FAQ

### What does "Slack whoami (signed-in account)" do?

Report which Slack account this browser is signed in as: the user's name, email, user id and the active workspace. Being signed out is reported as a normal answer (loggedIn false), not an error, so it can be used to check a session before running other Slack scripts.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns name, team, email, teamId, userId, teamUrl, evidence, loggedIn.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/whoami, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/whoami

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/whoami
