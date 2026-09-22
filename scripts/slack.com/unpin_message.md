# Slack API: unpin a message

Automatically unpin a message on slack.com. An unofficial Slack API: unpin a Slack message programmatically, from code or from an AI agent, with typed JSON in and out. It needs no Slack app or token, only your signed-in browser.

- Site: slack.com
- Address: `reduck/slack.com/unpin_message`
- Updated: 2026-09-18 (v4)
- Author: Reduck AI (reduck)

## About

Developers looking for a Slack API to unpin a Slack message usually find there is none they can use: it needs no Slack app or token, only your signed-in browser. This script fills that gap. It works like an API endpoint — one call with typed arguments, a JSON response — but runs through a real browser, yours or a hosted one, so it needs no Slack developer account, API key or app review.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/unpin_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/unpin_message
```

## Input

- `ts` (string, required): The message's ts.
- `channel` (string, required): Channel name/#name or id (C…).
- `workspaceDomain` (string, optional): Workspace host, e.g. acme.slack.com. Defaults to the active workspace.

## Output

- `ok` (boolean, required)
- `ts` (string, required)
- `channel` (string, required): Resolved channel id.
- `account_used` (string, required): Workspace host the action ran against, read back from the session.
- `already_absent` (boolean, required): True when the message was already not pinned before this run, so nothing changed.
- `verified_on_page` (boolean, required): True when a re-read of the channel's pins confirms the message is no longer pinned.
- `channel_name` (string | null, optional): Resolved channel name, when Slack reports one.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "ok": true,
  "ts": "…",
  "channel": "…",
  "account_used": "…",
  "channel_name": "…",
  "already_absent": true,
  "verified_on_page": true
}
```

## FAQ

### What does "Slack API: unpin a message" do?

Remove a pinned message from its channel by channel (name or id) and message ts. Requires login.

### How do I automatically unpin a message on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/unpin_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/unpin_message

### Is there a slack.com API to unpin a message?

You do not need one. "Slack API: unpin a message" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, ts. Optional: workspaceDomain.

### What does it return?

It returns ok, ts, channel, account_used, channel_name, already_absent, verified_on_page.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/unpin_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/unpin_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Is there a Slack API to unpin a Slack message?

Not an official one you can use for this: it needs no Slack app or token, only your signed-in browser. This script works as an unofficial Slack API for it: typed input, JSON output, callable from an AI agent over MCP, from the CLI, or over REST.

### How do I unpin a Slack message programmatically?

Call this script with its arguments and read the JSON it returns. It drives Slack in a real browser session, so there is no API key to request and nothing to reverse-engineer yourself.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/unpin_message
