# Get Slack user presence

Automatically get Slack user presence on slack.com. Get a Slack user's presence (active or away) and display name, by user id (U…), shown beside a channel or DM the signed-in account is in. Fails if the user is not in the workspace or the channel cannot be opened. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/get_user_presence`
- Updated: 2026-11-05 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/get_user_presence`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/get_user_presence
```

## Input

- `user` (string, required): Slack user id (U…). It is on the user's profile, under the more actions menu (Copy member ID).
- `channel` (string, required): Id (C…, G… or D…) of a channel or DM the signed-in account is in; the profile opens beside it. Get it from the channel's details (bottom of the About tab) or from the conversation URL in Slack (…/client/T…/<id>).
- `workspaceDomain` (string, required): Workspace host, e.g. acme.slack.com.

## Output

- `user` (string, required)
- `presence` (string, required)
- `userName` (string | null, optional)

## FAQ

### What does "Get Slack user presence" do?

Get a Slack user's presence (active or away) and display name, by user id (U…), shown beside a channel or DM the signed-in account is in. Fails if the user is not in the workspace or the channel cannot be opened. Requires login.

### How do I automatically get Slack user presence on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_user_presence, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_user_presence

### Is there a slack.com API to get Slack user presence?

You do not need one. "Get Slack user presence" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: user, channel, workspaceDomain.

### What does it return?

It returns user, presence, userName.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/get_user_presence, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/get_user_presence

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/get_user_presence
