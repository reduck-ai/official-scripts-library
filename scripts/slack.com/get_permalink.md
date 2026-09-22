# Get Slack message permalink

Automatically get Slack message permalink on slack.com. Get the shareable permalink URL for a message by channel (name or id) and message ts. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/get_permalink`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/get_permalink`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/get_permalink
```

## Input

- `ts` (string, required): The message's ts.
- `channel` (string, required): Channel name/#name or id (C…).
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `permalink` (string, required)
- `ts` (string, optional)
- `channel` (string, optional)

## FAQ

### What does "Get Slack message permalink" do?

Get the shareable permalink URL for a message by channel (name or id) and message ts. Requires login.

### How do I automatically get Slack message permalink on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_permalink, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_permalink

### Is there a slack.com API to get Slack message permalink?

You do not need one. "Get Slack message permalink" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, ts. Optional: workspaceDomain.

### What does it return?

It returns ok, ts, channel, permalink.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

Unknown: its author has not declared whether it changes anything on slack.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_permalink, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_permalink

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/get_permalink
