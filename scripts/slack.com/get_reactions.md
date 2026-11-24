# Get Slack message reactions

Automatically get Slack message reactions on slack.com. List the reactions on a message by channel (name or id) and message ts: each emoji with its count and the display names of who reacted. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/get_reactions`
- Updated: 2026-11-23 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/get_reactions`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/get_reactions
```

## Input

- `ts` (string, required): The message's ts.
- `channel` (string, required): Channel or DM id (C…/D…/G…). Get it from slack.com/list_channels.
- `workspaceDomain` (string, required): Workspace host, e.g. acme.slack.com.

## Output

- `ts` (string, required)
- `channel` (string, required)
- `reactions` (array, required)
- `workspace` (string, optional)

## FAQ

### What does "Get Slack message reactions" do?

List the reactions on a message by channel (name or id) and message ts: each emoji with its count and the display names of who reacted. Requires login.

### How do I automatically get Slack message reactions on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_reactions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_reactions

### Is there a slack.com API to get Slack message reactions?

You do not need one. "Get Slack message reactions" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, ts, workspaceDomain.

### What does it return?

It returns ts, channel, reactions, workspace.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_reactions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_reactions

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/get_reactions
