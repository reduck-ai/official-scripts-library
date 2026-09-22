# Get Slack user presence

Automatically get Slack user presence on slack.com. Get a user's presence (active/away) by id (U…) or @handle, plus their display name. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/get_user_presence`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/get_user_presence`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/get_user_presence
```

## Input

- `user` (string, required): User id (U…) or @handle.
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `user` (string, required)
- `presence` (string, required)
- `userName` (string | null, optional)

## FAQ

### What does "Get Slack user presence" do?

Get a user's presence (active/away) by id (U…) or @handle, plus their display name. Requires login.

### How do I automatically get Slack user presence on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_user_presence, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_user_presence

### Is there a slack.com API to get Slack user presence?

You do not need one. "Get Slack user presence" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: user. Optional: workspaceDomain.

### What does it return?

It returns user, presence, userName.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

Unknown: its author has not declared whether it changes anything on slack.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_user_presence, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_user_presence

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/get_user_presence
