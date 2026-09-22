# Get Telegram conversation

Automatically get Telegram conversation on web.telegram.org. Open one Telegram conversation by its peer id (the id get_inbox returns) and read its messages in chronological order: message id, text, the time shown on the bubble, whether it carries media, and — for channel posts — the exact view and forward counts. Scrolls upward to load older messages up to the requested count. Returns an empty list for a conversation with no messages, which is a real answer rather than a failure.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/get_conversation`
- Updated: 2026-09-16 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/get_conversation`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_conversation
```

## Input

- `peerId` (string, required): The conversation's peer id, as returned by get_inbox (e.g. "-1001928149680"). Passed straight to Telegram's own deep link, so it must be the id and not a display name.
- `count` (integer, optional): How many of the most recent messages to return, scrolling upward to load older ones.

## Output

- `count` (integer, required): How many messages were returned.
- `state` (string, required): "ready" when message bubbles rendered; "empty" for a conversation that resolved (it has a title) but holds no messages — only after the empty list has held steady long enough to rule out a list that is still loading. An unresolvable peer id throws instead.
- `peerId` (string, required): The peer id that was actually opened, read back from the address bar.
- `messages` (array, required): Messages oldest-first, as the conversation displays them.
- `chatTitle` (string | null, optional): The conversation title shown in the header, for a human-readable cross-check against peerId.

## FAQ

### What does "Get Telegram conversation" do?

Open one Telegram conversation by its peer id (the id get_inbox returns) and read its messages in chronological order: message id, text, the time shown on the bubble, whether it carries media, and — for channel posts — the exact view and forward counts. Scrolls upward to load older messages up to the requested count. Returns an empty list for a conversation with no messages, which is a real answer rather than a failure.

### How do I automatically get Telegram conversation on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_conversation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_conversation

### Is there a web.telegram.org API to get Telegram conversation?

You do not need one. "Get Telegram conversation" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Required: peerId. Optional: count.

### What does it return?

It returns count, state, peerId, messages, chatTitle.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It only reads. It looks things up on web.telegram.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_conversation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_conversation

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/get_conversation
