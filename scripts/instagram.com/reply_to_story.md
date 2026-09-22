# Reply to Instagram story

Automatically reply to Instagram story on instagram.com. Send a text reply to a user's currently-active Instagram story, delivered as a DM. Takes the story owner's username (trimmed, lower-cased and de-@'d for you) and the reply text; returns the sent message's id. The three failure modes are reported distinctly rather than lumped together: no such account, the account has no active story, and the current slide doesn't accept replies (e.g. a shared reel or a link-sticker slide).

- Site: instagram.com
- Address: `reduck/instagram.com/reply_to_story`
- Updated: 2026-09-21 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/reply_to_story`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/reply_to_story
```

## Input

- `text` (string, required): Reply text to send.
- `username` (string, required): Instagram username whose active story to reply to.

## Output

- `text` (string, required)
- `username` (string, required): The normalised username the reply was actually sent to (trimmed, lower-cased, no leading @).
- `message_id` (string, required): The sent DM message's id.
- `timestamp_ms` (string, required): Send timestamp in epoch milliseconds, as a string.

## FAQ

### What does "Reply to Instagram story" do?

Send a text reply to a user's currently-active Instagram story, delivered as a DM. Takes the story owner's username (trimmed, lower-cased and de-@'d for you) and the reply text; returns the sent message's id. The three failure modes are reported distinctly rather than lumped together: no such account, the account has no active story, and the current slide doesn't accept replies (e.g. a shared reel or a link-sticker slide).

### How do I automatically reply to Instagram story on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/reply_to_story, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/reply_to_story

### Is there a instagram.com API to reply to Instagram story?

You do not need one. "Reply to Instagram story" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username, text.

### What does it return?

It returns text, username, message_id, timestamp_ms.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/reply_to_story, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/reply_to_story

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/reply_to_story
