# Get Telegram inbox

Automatically get Telegram inbox on web.telegram.org. List the conversations in the Telegram Web chat list, newest first: each one's name, its peer id (the handle every other Telegram script uses to open it), the last message preview, the time shown on the row, and the unread count. Scrolls to load older conversations up to the requested count. Returns an empty list when the account has no conversations, which is a real answer rather than a failure.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/get_inbox`
- Updated: 2026-09-17 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/get_inbox`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_inbox
```

## Input

- `count` (integer, optional): Maximum conversations to return, scrolling the chat list to load older ones.
- `since` (string, optional): Optional ISO datetime. Return only conversations whose last activity is at or after this instant, which is how a caller polls for new messages. Conversations whose timestamp could not be resolved are always returned, never silently dropped.

## Output

- `chats` (array, required): Conversations in the order the chat list shows them (most recent activity first). Empty when the account has none.
- `count` (integer, required): How many conversations were returned.
- `state` (string, required): "ready" when the chat list rendered rows. "empty" when the app shell mounted and the chat list then STAYED empty for a hold period (4s with the list container mounted, 12s without), which is how an account with no conversations looks - reported rather than treated as a failure. The hold is what distinguishes it from an account still syncing, whose list fills during the hold; a run that never settles either way throws instead, as does being signed out, so neither can be confused with "empty". Renamed from "empty-or-syncing" in v2: that hedge existed only because v1 could not tell the two states apart.

## FAQ

### What does "Get Telegram inbox" do?

List the conversations in the Telegram Web chat list, newest first: each one's name, its peer id (the handle every other Telegram script uses to open it), the last message preview, the time shown on the row, and the unread count. Scrolls to load older conversations up to the requested count. Returns an empty list when the account has no conversations, which is a real answer rather than a failure.

### How do I automatically get Telegram inbox on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_inbox

### Is there a web.telegram.org API to get Telegram inbox?

You do not need one. "Get Telegram inbox" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Optional: count, since.

### What does it return?

It returns chats, count, state.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It only reads. It looks things up on web.telegram.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_inbox

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/get_inbox
