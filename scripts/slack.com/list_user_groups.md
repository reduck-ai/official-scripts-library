# List Slack user groups

Automatically list Slack user groups on slack.com. List the workspace's user groups (@-groups). Returns each group's id, handle, name, description and member count. Empty on plans without user groups. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/list_user_groups`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_user_groups`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_user_groups
```

## Input

- `includeDisabled` (boolean, optional): Include disabled groups. Default false.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `groups` (array, required)

## FAQ

### What does "List Slack user groups" do?

List the workspace's user groups (@-groups). Returns each group's id, handle, name, description and member count. Empty on plans without user groups. Requires login.

### How do I automatically list Slack user groups on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_user_groups, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_user_groups

### Is there a slack.com API to list Slack user groups?

You do not need one. "List Slack user groups" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Optional: includeDisabled, workspaceDomain.

### What does it return?

It returns groups.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

Unknown: its author has not declared whether it changes anything on slack.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_user_groups, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_user_groups

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_user_groups
