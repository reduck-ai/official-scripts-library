# Delete a Telegram message

Automatically delete a Telegram message on web.telegram.org. Delete one message from a Telegram conversation, by the conversation's peer id and the message id, and confirm with Telegram that this one message is gone. Deleting cannot be undone and, in a shared conversation, other people can see it: get the user's confirmation first, and show them the chatTitle this returns. Pass scope "everyone" to remove it for all participants, which Telegram offers only on this account's own recent messages. Refuses a message that does not exist.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/delete_message`
- Updated: 2026-11-11 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/delete_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/delete_message
```

## Input

- `peerId` (string, required): The conversation, as web.telegram.org/get_inbox returns it.
- `messageId` (string, required): The message to delete, as get_conversation, search_messages or send_message return it. It must be among the most recent messages of the conversation.
- `scope` (string, optional): "me" removes it for this account only. "everyone" removes it for all participants, which Telegram offers only on this account's own recent messages; the run fails rather than fall back to "me".

## Output

- `scope` (string, required)
- `peerId` (string, required)
- `deleted` (boolean, required): True once Telegram reports the message as deleted.
- `messageId` (string, required)
- `account_used` (string | null, required): The name of the account that deleted it.
- `accountId` (string, optional)
- `chatTitle` (string | null, optional): The conversation's name: show it to the user.

## FAQ

### What does "Delete a Telegram message" do?

Delete one message from a Telegram conversation, by the conversation's peer id and the message id, and confirm with Telegram that this one message is gone. Deleting cannot be undone and, in a shared conversation, other people can see it: get the user's confirmation first, and show them the chatTitle this returns. Pass scope "everyone" to remove it for all participants, which Telegram offers only on this account's own recent messages. Refuses a message that does not exist.

### How do I automatically delete a Telegram message on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/delete_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/delete_message

### Is there a web.telegram.org API to delete a Telegram message?

You do not need one. "Delete a Telegram message" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Required: peerId, messageId. Optional: scope.

### What does it return?

It returns scope, peerId, deleted, accountId, chatTitle, messageId, account_used.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It makes changes on web.telegram.org, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/delete_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/delete_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/delete_message
