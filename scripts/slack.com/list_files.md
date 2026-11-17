# List Slack files

Automatically list Slack files on slack.com. List files shared in the workspace, optionally filtered by channel (name or id) and/or uploader (user id). One page per call (count/page). Returns id, name, title, type, size, user, timestamp and permalink. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/list_files`
- Updated: 2026-11-16 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_files`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_files
```

## Input

- `workspaceDomain` (string, required): Workspace host, e.g. acme.slack.com, from slack.com/list_workspaces.
- `page` (integer, optional): 1-based page.
- `user` (string, optional): Only files from this uploader (user id U…). Optional.
- `count` (integer, optional): Files per page.
- `channel` (string, optional): Only files shared in this channel (id C…, from slack.com/list_channels). Optional.

## Output

- `files` (array, required)
- `page` (integer | null, optional)
- `total` (integer | null, optional)
- `pageCount` (integer | null, optional)

## FAQ

### What does "List Slack files" do?

List files shared in the workspace, optionally filtered by channel (name or id) and/or uploader (user id). One page per call (count/page). Returns id, name, title, type, size, user, timestamp and permalink. Requires login.

### How do I automatically list Slack files on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_files, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_files

### Is there a slack.com API to list Slack files?

You do not need one. "List Slack files" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: workspaceDomain. Optional: page, user, count, channel.

### What does it return?

It returns page, files, total, pageCount.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_files, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_files

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_files
