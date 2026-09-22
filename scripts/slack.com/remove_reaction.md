# Remove Slack reaction

Automatically remove Slack reaction on slack.com. Remove one of your emoji reactions from a message by channel (name or id) and message ts. Emoji name without colons. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/remove_reaction`
- Updated: 2026-07-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/remove_reaction`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/remove_reaction
```

## Input

- `ts` (string, required): The message's ts.
- `emoji` (string, required): Emoji name without colons, e.g. 'thumbsup'.
- `channel` (string, required): Channel name/#name or id (C…).
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `ts` (string, optional)
- `emoji` (string, optional)
- `channel` (string, optional)

## FAQ

### What does "Remove Slack reaction" do?

Remove one of your emoji reactions from a message by channel (name or id) and message ts. Emoji name without colons. Requires login.

### How do I automatically remove Slack reaction on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/remove_reaction, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/remove_reaction

### Is there a slack.com API to remove Slack reaction?

You do not need one. "Remove Slack reaction" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, ts, emoji. Optional: workspaceDomain.

### What does it return?

It returns ok, ts, emoji, channel.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/remove_reaction, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/remove_reaction

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/remove_reaction
