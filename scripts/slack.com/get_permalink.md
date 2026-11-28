# Get Slack message permalink

Automatically get Slack message permalink on slack.com. Get the shareable permalink URL for a Slack message from its workspace, channel (id or name) and message ts, after checking that the message is in that channel. Returns the channel id too. Works for top-level messages; thread replies are not supported. Requires being signed in to that workspace.

- Site: slack.com
- Address: `reduck/slack.com/get_permalink`
- Updated: 2026-11-24 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/get_permalink`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/get_permalink
```

## Input

- `ts` (string, required): The message's ts, e.g. 1793723772.371299.
- `channel` (string, required): Channel id (C…, G… or D…) or channel name, with or without #.
- `workspaceDomain` (string, required): Workspace host, e.g. acme.slack.com.

## Output

- `ok` (boolean, required)
- `permalink` (string, required)
- `ts` (string, optional)
- `channel` (string, optional): The channel id.

## FAQ

### What does "Get Slack message permalink" do?

Get the shareable permalink URL for a Slack message from its workspace, channel (id or name) and message ts, after checking that the message is in that channel. Returns the channel id too. Works for top-level messages; thread replies are not supported. Requires being signed in to that workspace.

### How do I automatically get Slack message permalink on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_permalink, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_permalink

### Is there a slack.com API to get Slack message permalink?

You do not need one. "Get Slack message permalink" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, ts, workspaceDomain.

### What does it return?

It returns ok, ts, channel, permalink.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for slack.com.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_permalink, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_permalink

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/get_permalink
