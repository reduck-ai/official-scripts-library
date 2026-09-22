# Open Slack DM

Automatically open Slack DM on slack.com. Open (or fetch) a direct message with one user, or a group DM with several, given as @handles or user ids (U…). Returns the conversation id you can then post to. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/open_dm`
- Updated: 2026-07-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/open_dm`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/open_dm
```

## Input

- `users` (array, required): One user for a DM, several for a group DM: @handles or ids (U…).
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `channel` (string, required)
- `alreadyOpen` (boolean | null, optional)

## FAQ

### What does "Open Slack DM" do?

Open (or fetch) a direct message with one user, or a group DM with several, given as @handles or user ids (U…). Returns the conversation id you can then post to. Requires login.

### How do I automatically open Slack DM on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/open_dm, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/open_dm

### Is there a slack.com API to open Slack DM?

You do not need one. "Open Slack DM" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: users. Optional: workspaceDomain.

### What does it return?

It returns ok, channel, alreadyOpen.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/open_dm, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/open_dm

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/open_dm
