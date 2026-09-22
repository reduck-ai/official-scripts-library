# Pin Slack message

Automatically pin Slack message on slack.com. Pin a message to its Slack channel, given the channel (name or id) and the message ts. Safe to repeat: if the message is already pinned it reports success and tells you nothing changed. Confirms the pin afterwards and reports which workspace it acted on. Pinning is not possible in an archived channel, or in a channel the signed-in account has not joined — both are reported as such. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/pin_message`
- Updated: 2026-08-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/pin_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/pin_message
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
- `already_present` (boolean, required): True when the message was already pinned before this run, so nothing changed.
- `verified_on_page` (boolean, required): True when a re-read of the channel's pins confirms the message is pinned.
- `channel_name` (string | null, optional): Resolved channel name, when Slack reports one.

## FAQ

### What does "Pin Slack message" do?

Pin a message to its Slack channel, given the channel (name or id) and the message ts. Safe to repeat: if the message is already pinned it reports success and tells you nothing changed. Confirms the pin afterwards and reports which workspace it acted on. Pinning is not possible in an archived channel, or in a channel the signed-in account has not joined — both are reported as such. Requires login.

### How do I automatically pin Slack message on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/pin_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/pin_message

### Is there a slack.com API to pin Slack message?

You do not need one. "Pin Slack message" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, ts. Optional: workspaceDomain.

### What does it return?

It returns ok, ts, channel, account_used, channel_name, already_present, verified_on_page.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/pin_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/pin_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/pin_message
