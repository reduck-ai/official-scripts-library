# Get Telegram conversation

Automatically get Telegram conversation on web.telegram.org. Read the messages of one Telegram conversation, 40 at a time, oldest first: id, date, sender, text, media kind, reply link and, for channel posts, exact view and forward counts. Takes a peer id from get_inbox, or a public @username, which reads a public channel without joining it. Pass nextBeforeMessageId to read older messages. Reading does not mark the conversation as read. A conversation with no messages returns an empty list.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/get_conversation`
- Updated: 2026-11-11 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/get_conversation`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_conversation
```

## Input

- `peerId` (string, required): The conversation: its peerId from web.telegram.org/get_inbox (a signed integer, e.g. "-1001005640892"), or the public username of a channel, group or person (e.g. "@telegram"), which works without joining it.
- `beforeMessageId` (string, optional): Omit for the most recent messages. To read older ones, pass the nextBeforeMessageId of the previous call.

## Output

- `peerId` (string, required): The conversation's peer id (also when a username was passed).
- `messages` (array, required): Up to 40 messages, oldest first. Empty for a conversation with no messages.
- `nextBeforeMessageId` (string | null, required): Pass it as beforeMessageId to read the page of older messages. Null when this page reaches the first message.
- `kind` (string, optional)
- `title` (string | null, optional): The conversation's name.
- `totalCount` (integer | null, optional): How many messages the conversation holds in all.

## FAQ

### What does "Get Telegram conversation" do?

Read the messages of one Telegram conversation, 40 at a time, oldest first: id, date, sender, text, media kind, reply link and, for channel posts, exact view and forward counts. Takes a peer id from get_inbox, or a public @username, which reads a public channel without joining it. Pass nextBeforeMessageId to read older messages. Reading does not mark the conversation as read. A conversation with no messages returns an empty list.

### How do I automatically get Telegram conversation on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_conversation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_conversation

### Is there a web.telegram.org API to get Telegram conversation?

You do not need one. "Get Telegram conversation" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Required: peerId. Optional: beforeMessageId.

### What does it return?

It returns kind, title, peerId, messages, totalCount, nextBeforeMessageId.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It only reads. It looks things up on web.telegram.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_conversation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_conversation

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/get_conversation
