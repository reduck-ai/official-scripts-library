# Set Slack Do-Not-Disturb

Automatically set Slack Do-Not-Disturb on slack.com. Snooze notifications for N minutes, or end an active snooze with minutes = 0. Returns the snooze state. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/set_dnd`
- Updated: 2026-07-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/set_dnd`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/set_dnd
```

## Input

- `minutes` (integer, required): Minutes to snooze. 0 ends the current snooze.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `snoozeEnabled` (boolean, required)
- `snoozeEndtime` (integer | null, optional)

## FAQ

### What does "Set Slack Do-Not-Disturb" do?

Snooze notifications for N minutes, or end an active snooze with minutes = 0. Returns the snooze state. Requires login.

### How do I automatically set Slack Do-Not-Disturb on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/set_dnd, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/set_dnd

### Is there a slack.com API to set Slack Do-Not-Disturb?

You do not need one. "Set Slack Do-Not-Disturb" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: minutes. Optional: workspaceDomain.

### What does it return?

It returns ok, snoozeEnabled, snoozeEndtime.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/set_dnd, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/set_dnd

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/set_dnd
