# Get Slack channel messages

Automatically get Slack channel messages on slack.com. Read the latest messages of a Slack channel by its id (C…, G… or D…), as the Slack app loads them when the channel is opened: one page of recent history, in Slack's own order. Authors are resolved to display names. Opening the channel does not mark it read. Requires being signed in to that workspace.

- Site: slack.com
- Address: `reduck/slack.com/get_channel_messages`
- Updated: 2026-11-24 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/get_channel_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/get_channel_messages
```

## Input

- `channel` (string, required): Channel id (C…, G… or D…), as listed by slack.com/list_channels.
- `workspaceDomain` (string, required): Workspace host, e.g. acme.slack.com.

## Output

- `channel` (string, required)
- `messages` (array, required)
- `nextCursor` (string | null, optional)

## FAQ

### What does "Get Slack channel messages" do?

Read the latest messages of a Slack channel by its id (C…, G… or D…), as the Slack app loads them when the channel is opened: one page of recent history, in Slack's own order. Authors are resolved to display names. Opening the channel does not mark it read. Requires being signed in to that workspace.

### How do I automatically get Slack channel messages on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_channel_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_channel_messages

### Is there a slack.com API to get Slack channel messages?

You do not need one. "Get Slack channel messages" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, workspaceDomain.

### What does it return?

It returns channel, messages, nextCursor.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for slack.com.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_channel_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_channel_messages

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/get_channel_messages
