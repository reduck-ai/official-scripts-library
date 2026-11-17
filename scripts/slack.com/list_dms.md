# List Slack direct messages

Automatically list Slack direct messages on slack.com. List the direct-message and group-DM conversations that Slack's DMs view shows, each with the counterpart's display name when Slack provides it and the last message. One page per call; pass cursor to paginate when Slack returns one. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/list_dms`
- Updated: 2026-11-16 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_dms`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_dms
```

## Input

- `workspaceDomain` (string, required): Workspace host, e.g. acme.slack.com, from slack.com/list_workspaces.
- `limit` (integer, optional): Max conversations per page.
- `cursor` (string, optional): nextCursor from a previous call.

## Output

- `dms` (array, required)
- `workspace` (string, required)
- `nextCursor` (string | null, optional)

## FAQ

### What does "List Slack direct messages" do?

List the direct-message and group-DM conversations that Slack's DMs view shows, each with the counterpart's display name when Slack provides it and the last message. One page per call; pass cursor to paginate when Slack returns one. Requires login.

### How do I automatically list Slack direct messages on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_dms, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_dms

### Is there a slack.com API to list Slack direct messages?

You do not need one. "List Slack direct messages" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: workspaceDomain. Optional: limit, cursor.

### What does it return?

It returns dms, workspace, nextCursor.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_dms, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_dms

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_dms
