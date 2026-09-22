# Get Slack channel info

Automatically get Slack channel info on slack.com. Get one channel's details by name or id: name, privacy, member count, topic, purpose, creator, created date, and archived/general flags. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/get_channel_info`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/get_channel_info`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/get_channel_info
```

## Input

- `channel` (string, required): Channel name/#name or id (C…).
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `id` (string, required)
- `name` (string | null, required)
- `topic` (string | null, optional)
- `created` (integer | null, optional)
- `creator` (string | null, optional)
- `purpose` (string | null, optional)
- `is_member` (boolean, optional)
- `is_general` (boolean, optional)
- `is_private` (boolean, optional)
- `is_archived` (boolean, optional)
- `num_members` (integer | null, optional)

## FAQ

### What does "Get Slack channel info" do?

Get one channel's details by name or id: name, privacy, member count, topic, purpose, creator, created date, and archived/general flags. Requires login.

### How do I automatically get Slack channel info on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_channel_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_channel_info

### Is there a slack.com API to get Slack channel info?

You do not need one. "Get Slack channel info" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel. Optional: workspaceDomain.

### What does it return?

It returns id, name, topic, created, creator, purpose, is_member, is_general, is_private, is_archived, num_members.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

Unknown: its author has not declared whether it changes anything on slack.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_channel_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_channel_info

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/get_channel_info
