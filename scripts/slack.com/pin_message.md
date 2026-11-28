# Pin Slack message

Automatically pin Slack message on slack.com. Pin a message in a Slack channel, given the channel id and the message ts. Safe to repeat: an already pinned message reports already_present. Fails with a clear message for an archived channel or one the account has not joined.

- Site: slack.com
- Address: `reduck/slack.com/pin_message`
- Updated: 2026-11-24 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/pin_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/pin_message
```

## Input

- `ts` (string, required): The message's ts.
- `channel` (string, required): Channel id (C… or G…), e.g. from the channel's link.
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

Pin a message in a Slack channel, given the channel id and the message ts. Safe to repeat: an already pinned message reports already_present. Fails with a clear message for an archived channel or one the account has not joined.

### How do I automatically pin Slack message on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/pin_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/pin_message

### Is there a slack.com API to pin Slack message?

You do not need one. "Pin Slack message" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, ts. Optional: workspaceDomain.

### What does it return?

It returns ok, ts, channel, account_used, channel_name, already_present, verified_on_page.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for slack.com.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/pin_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/pin_message

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/pin_message
