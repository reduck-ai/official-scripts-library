# Get Instagram DM inbox

Automatically get Instagram DM inbox on instagram.com. List the state of every DM conversation in your Instagram inbox. count=0 fetches every page. Returns count, unseen_count, and threads (thread_id, title, users, is_group, unread, last_activity_at, last_activity (ISO), last_message). Each last_message has sent_by_me (you vs them), date (ISO), type, and text. thread_id is the join key for reading a conversation's messages.

- Site: instagram.com
- Address: `reduck/instagram.com/get_inbox`
- Updated: 2026-09-17 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_inbox`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_inbox
```

## Input

- `count` (number, optional): Max conversations to fetch; 0 = every page Instagram serves.
- `since` (string, optional): Optional ISO datetime. Return only conversations whose last activity is at or after this instant, and stop paginating once older activity is reached — this is how a caller polls for new messages. Threads with no resolvable timestamp are always returned, never silently dropped.

## Output

- `count` (number, required)
- `threads` (array, required)
- `unseen_count` (number | null, optional)
- `reached_since` (boolean | null, optional): Only set when `since` was given. True means pagination walked back past the cutoff, so every conversation newer than it was seen. False means the inbox was exhausted (or no older page existed) first.

## FAQ

### What does "Get Instagram DM inbox" do?

List the state of every DM conversation in your Instagram inbox. count=0 fetches every page. Returns count, unseen_count, and threads (thread_id, title, users, is_group, unread, last_activity_at, last_activity (ISO), last_message). Each last_message has sent_by_me (you vs them), date (ISO), type, and text. thread_id is the join key for reading a conversation's messages.

### How do I automatically get Instagram DM inbox on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_inbox

### Is there a instagram.com API to get Instagram DM inbox?

You do not need one. "Get Instagram DM inbox" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Optional: count, since.

### What does it return?

It returns count, threads, unseen_count, reached_since.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_inbox

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_inbox
