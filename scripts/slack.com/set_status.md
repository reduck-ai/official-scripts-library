# Set Slack status

Automatically set Slack status on slack.com. Set your own Slack status: text plus an emoji (with colons, e.g. ':coffee:'), optionally auto-clearing after expireInMinutes. Pass empty text to clear. Returns the applied status. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/set_status`
- Updated: 2026-07-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/set_status`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/set_status
```

## Input

- `text` (string, optional): Status text. Empty string clears the status.
- `emoji` (string, optional): Status emoji with colons, e.g. ':coffee:'. Optional.
- `expireInMinutes` (integer, optional): Auto-clear after N minutes. 0 or omitted = no expiry.
- `workspaceDomain` (string, optional): Workspace host. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `status_text` (string | null, optional)
- `status_emoji` (string | null, optional)
- `status_expiration` (integer | null, optional)

## FAQ

### What does "Set Slack status" do?

Set your own Slack status: text plus an emoji (with colons, e.g. ':coffee:'), optionally auto-clearing after expireInMinutes. Pass empty text to clear. Returns the applied status. Requires login.

### How do I automatically set Slack status on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/set_status, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/set_status

### Is there a slack.com API to set Slack status?

You do not need one. "Set Slack status" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Optional: text, emoji, expireInMinutes, workspaceDomain.

### What does it return?

It returns ok, status_text, status_emoji, status_expiration.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/set_status, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/set_status

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/set_status
