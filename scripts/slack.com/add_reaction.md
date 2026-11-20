# Add Slack reaction

Automatically add Slack reaction on slack.com. Add an emoji reaction to a Slack message by channel id and message ts. Emoji name without colons. Returns alreadyPresent true and changes nothing when this account already left that reaction. Fails when the channel or message is not found.

- Site: slack.com
- Address: `reduck/slack.com/add_reaction`
- Updated: 2026-11-19 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/add_reaction`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/add_reaction
```

## Input

- `ts` (string, required): The message's ts.
- `emoji` (string, required): Emoji name without colons, e.g. 'thumbsup', 'white_check_mark'. Aliases are accepted; the output gives the name Slack stores.
- `channel` (string, required): Channel or DM id (C…/D…/G…). Get it from slack.com/list_channels.
- `workspaceDomain` (string, required): Workspace host, e.g. acme.slack.com. Confirm with the user which workspace to target before running.

## Output

- `ok` (boolean, required)
- `ts` (string, required)
- `emoji` (string, required): The emoji name Slack stores, e.g. '+1' for 'thumbsup'.
- `channel` (string, required)
- `workspace` (string, optional)
- `alreadyPresent` (boolean, optional)

## FAQ

### What does "Add Slack reaction" do?

Add an emoji reaction to a Slack message by channel id and message ts. Emoji name without colons. Returns alreadyPresent true and changes nothing when this account already left that reaction. Fails when the channel or message is not found.

### How do I automatically add Slack reaction on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/add_reaction, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/add_reaction

### Is there a slack.com API to add Slack reaction?

You do not need one. "Add Slack reaction" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, ts, emoji, workspaceDomain.

### What does it return?

It returns ok, ts, emoji, channel, workspace, alreadyPresent.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/add_reaction, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/add_reaction

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/add_reaction
