# Get Telegram inbox

Automatically get Telegram inbox on web.telegram.org. List the conversations in the Telegram Web chat list, newest first: each one's name, its peer id (the handle every other Telegram script uses to open it), the last message preview, the time shown on the row, and the unread count. Scrolls to load older conversations up to the requested count. Returns an empty list when the account has no conversations, which is a real answer rather than a failure.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/get_inbox`
- Updated: 2026-10-29 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/get_inbox`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_inbox
```

## Input

- `count` (integer, optional): Maximum conversations to return, scrolling the chat list to load older ones.

## Output

- `chats` (array, required)
- `count` (integer, required)
- `state` (string, required)
- `complete` (boolean, required): True when every conversation of the chat list was returned; false when count stopped the list first.

## FAQ

### What does "Get Telegram inbox" do?

List the conversations in the Telegram Web chat list, newest first: each one's name, its peer id (the handle every other Telegram script uses to open it), the last message preview, the time shown on the row, and the unread count. Scrolls to load older conversations up to the requested count. Returns an empty list when the account has no conversations, which is a real answer rather than a failure.

### How do I automatically get Telegram inbox on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_inbox

### Is there a web.telegram.org API to get Telegram inbox?

You do not need one. "Get Telegram inbox" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Optional: count.

### What does it return?

It returns chats, count, state, complete.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It only reads. It looks things up on web.telegram.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_inbox

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/get_inbox
