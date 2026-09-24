# Export a Slack conversation to a JSON file

Automatically export a Slack conversation to a JSON file on slack.com. Downloads the full accessible history of one Slack conversation as a JSON file, including thread replies. Works for a channel, a direct message, a group message or your own saved messages, addressed by name, by ID or by the other person's handle.

- Site: slack.com
- Address: `reduck/slack.com/export_conversation`
- Updated: 2026-09-23 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/export_conversation`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/export_conversation
```

## Input

- `conversation` (string, required): What to export. A channel as '#general' or 'general'; any conversation by its ID (C, G or D prefix); a direct message as '@handle' or the other person's user ID; or 'self' for your own saved messages. Display names are rejected because several people can share one, so use a handle or an ID.
- `expectedUser` (string, required): Your Slack handle, display name, or user ID. Checked against the signed-in account before anything is exported.
- `workspaceDomain` (string, required): Workspace hostname, for example acme.slack.com.
- `maxPages` (integer, optional): Safety cap across history and reply pages. Exceeding it fails rather than downloading a partial archive.
- `inspectOnly` (boolean, optional): Resolve and report the workspace, account and conversation without reading history or downloading anything.

## Output

- `account` (object, required)
- `workspace` (string, required)
- `conversationId` (string, required)
- `inspectionOnly` (boolean, required)
- `conversationType` (string, required)
- `download` (object, optional)
- `pageCount` (integer, optional)
- `threadCount` (integer, optional)
- `counterparty` (object | null, optional)
- `messageCount` (integer, optional)
- `lastTimestamp` (string | null, optional)
- `firstTimestamp` (string | null, optional)
- `conversationName` (string | null, optional)
- `completeForAccessibleHistory` (boolean, optional)

## FAQ

### What does "Export a Slack conversation to a JSON file" do?

Downloads the full accessible history of one Slack conversation as a JSON file, including thread replies. Works for a channel, a direct message, a group message or your own saved messages, addressed by name, by ID or by the other person's handle.

### How do I automatically export a Slack conversation to a JSON file on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/export_conversation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/export_conversation

### Is there a slack.com API to export a Slack conversation to a JSON file?

You do not need one. "Export a Slack conversation to a JSON file" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: workspaceDomain, expectedUser, conversation. Optional: maxPages, inspectOnly.

### What does it return?

It returns account, download, pageCount, workspace, threadCount, counterparty, messageCount, lastTimestamp, conversationId, firstTimestamp, inspectionOnly, conversationName, conversationType, completeForAccessibleHistory.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/export_conversation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/export_conversation

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/export_conversation
