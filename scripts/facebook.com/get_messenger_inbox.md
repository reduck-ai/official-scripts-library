# List Facebook Messenger conversations

Automatically list Facebook Messenger conversations on facebook.com. List the most recent conversations of the signed-in Facebook account's Messenger inbox: id, link, name, the other participants, whether it is a group, the latest message preview, the time of the latest activity and whether it is unread. Reading the list marks nothing as read. Facebook serves around 30 conversations with the page; limit caps how many are returned and served says how many were available. End-to-end encrypted conversations are listed without a preview. Works in any interface language.

- Site: facebook.com
- Address: `reduck/facebook.com/get_messenger_inbox`
- Updated: 2026-11-13 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/get_messenger_inbox`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_messenger_inbox
```

## Input

- `limit` (integer, optional): Maximum number of conversations to return, most recent first.

## Output

- `served` (integer, required): How many conversations Facebook served with the page (the most recent ones, usually around 30). The inbox can hold more.
- `conversations` (array, required)

## FAQ

### What does "List Facebook Messenger conversations" do?

List the most recent conversations of the signed-in Facebook account's Messenger inbox: id, link, name, the other participants, whether it is a group, the latest message preview, the time of the latest activity and whether it is unread. Reading the list marks nothing as read. Facebook serves around 30 conversations with the page; limit caps how many are returned and served says how many were available. End-to-end encrypted conversations are listed without a preview. Works in any interface language.

### How do I automatically list Facebook Messenger conversations on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/get_messenger_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_messenger_inbox

### Is there a facebook.com API to list Facebook Messenger conversations?

You do not need one. "List Facebook Messenger conversations" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Optional: limit.

### What does it return?

It returns served, conversations.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/get_messenger_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/get_messenger_inbox

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/get_messenger_inbox
