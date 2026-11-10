# List Slack custom emoji

Automatically list Slack custom emoji on slack.com. List the workspace's own custom emoji as a name to URL map (aliases point to 'alias:<name>'), with count, total and whether the list is complete (the first 100 only). Requires login and the workspace host.

- Site: slack.com
- Address: `reduck/slack.com/list_custom_emoji`
- Updated: 2026-11-09 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_custom_emoji`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_custom_emoji
```

## Input

- `workspaceDomain` (string, required): Workspace host, e.g. acme.slack.com.

## Output

- `count` (integer, required)
- `emoji` (object, required)
- `total` (integer | null, optional)
- `complete` (boolean, optional)

## FAQ

### What does "List Slack custom emoji" do?

List the workspace's own custom emoji as a name to URL map (aliases point to 'alias:<name>'), with count, total and whether the list is complete (the first 100 only). Requires login and the workspace host.

### How do I automatically list Slack custom emoji on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_custom_emoji, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_custom_emoji

### Is there a slack.com API to list Slack custom emoji?

You do not need one. "List Slack custom emoji" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: workspaceDomain.

### What does it return?

It returns count, emoji, total, complete.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_custom_emoji, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_custom_emoji

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_custom_emoji
