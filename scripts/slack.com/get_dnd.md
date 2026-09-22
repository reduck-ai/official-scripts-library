# Get Slack Do-Not-Disturb

Automatically get Slack Do-Not-Disturb on slack.com. Get your (or another user's) Do-Not-Disturb state: whether DND is on, its scheduled window, and any active snooze. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/get_dnd`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/get_dnd`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/get_dnd
```

## Input

- `user` (string, optional): User id (U…) or @handle. Defaults to yourself.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `dndEnabled` (boolean, required)
- `nextEnd` (integer | null, optional)
- `nextStart` (integer | null, optional)
- `snoozeEnabled` (boolean, optional)
- `snoozeEndtime` (integer | null, optional)

## FAQ

### What does "Get Slack Do-Not-Disturb" do?

Get your (or another user's) Do-Not-Disturb state: whether DND is on, its scheduled window, and any active snooze. Requires login.

### How do I automatically get Slack Do-Not-Disturb on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_dnd, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_dnd

### Is there a slack.com API to get Slack Do-Not-Disturb?

You do not need one. "Get Slack Do-Not-Disturb" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Optional: user, workspaceDomain.

### What does it return?

It returns nextEnd, nextStart, dndEnabled, snoozeEnabled, snoozeEndtime.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

Unknown: its author has not declared whether it changes anything on slack.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_dnd, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_dnd

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/get_dnd
