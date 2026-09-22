# Get Instagram DM messages

Automatically get Instagram DM messages on instagram.com. Read the messages of a DM conversation by thread_id (get the thread_id from get_inbox). count=0 fetches every page. Returns thread_id, title, users, count, and messages in chronological order (oldest to newest), each with sent_by_me, sender, type, text, timestamp, and date (ISO). Timestamps are microsecond epochs; text is null for non-text items (use type, e.g. clip/media_share/like/action_log); sender is null for your own messages (sent_by_me=true).

- Site: instagram.com
- Address: `reduck/instagram.com/get_dm_messages`
- Updated: 2026-09-15 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_dm_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_dm_messages
```

## Input

- `thread_id` (string, required)
- `count` (number, optional)

## Output

- `count` (number, required)
- `users` (array, required)
- `messages` (array, required)
- `thread_id` (string, required)
- `last_seen_at` (array, required): Per-participant read position for the thread, as Instagram reports it. Empty when Instagram returns none.
- `title` (string | null, optional)

## FAQ

### What does "Get Instagram DM messages" do?

Read the messages of a DM conversation by thread_id (get the thread_id from get_inbox). count=0 fetches every page. Returns thread_id, title, users, count, and messages in chronological order (oldest to newest), each with sent_by_me, sender, type, text, timestamp, and date (ISO). Timestamps are microsecond epochs; text is null for non-text items (use type, e.g. clip/media_share/like/action_log); sender is null for your own messages (sent_by_me=true).

### How do I automatically get Instagram DM messages on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_dm_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_dm_messages

### Is there a instagram.com API to get Instagram DM messages?

You do not need one. "Get Instagram DM messages" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: thread_id. Optional: count.

### What does it return?

It returns count, title, users, messages, thread_id, last_seen_at.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_dm_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_dm_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_dm_messages
