# Get Slack workspace info

Automatically get Slack workspace info on slack.com. Get the current workspace's identity: id, name, url domain, email domain and icon URL. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/team_info`
- Updated: 2026-07-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/team_info`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/team_info
```

## Input

- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `id` (string, required)
- `name` (string | null, required)
- `icon` (string | null, optional)
- `domain` (string | null, optional)
- `emailDomain` (string | null, optional)

## FAQ

### What does "Get Slack workspace info" do?

Get the current workspace's identity: id, name, url domain, email domain and icon URL. Requires login.

### How do I automatically get Slack workspace info on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/team_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/team_info

### Is there a slack.com API to get Slack workspace info?

You do not need one. "Get Slack workspace info" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Optional: workspaceDomain.

### What does it return?

It returns id, icon, name, domain, emailDomain.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

Unknown: its author has not declared whether it changes anything on slack.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/team_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/team_info

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/team_info
