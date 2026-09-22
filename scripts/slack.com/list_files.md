# List Slack files

Automatically list Slack files on slack.com. List files shared in the workspace, optionally filtered by channel (name or id) and/or uploader (user id). One page per call (count/page). Returns id, name, title, type, size, user, timestamp and permalink. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/list_files`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_files`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_files
```

## Input

- `page` (integer, optional): 1-based page (default 1).
- `user` (string, optional): Filter to an uploader (user id U…). Optional.
- `count` (integer, optional): Files per page (default 50).
- `channel` (string, optional): Filter to a channel (name/id). Optional.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `files` (array, required)
- `total` (integer | null, optional)

## FAQ

### What does "List Slack files" do?

List files shared in the workspace, optionally filtered by channel (name or id) and/or uploader (user id). One page per call (count/page). Returns id, name, title, type, size, user, timestamp and permalink. Requires login.

### How do I automatically list Slack files on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_files, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_files

### Is there a slack.com API to list Slack files?

You do not need one. "List Slack files" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Optional: page, user, count, channel, workspaceDomain.

### What does it return?

It returns files, total.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

Unknown: its author has not declared whether it changes anything on slack.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_files, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_files

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_files
