# Read a TikTok direct message conversation

Automatically read a TikTok direct message conversation on tiktok.com. Read the messages in one of the signed-in account's direct message threads, addressed either by the other person's @username or by the conversation id the inbox script returns. Messages come back oldest to newest with the timestamp labels TikTok shows between them, and system notices in the thread (such as a message request being accepted) are marked as notices rather than passed off as messages. Opening a thread marks it as read, which is what the site does too. Pairs with the inbox script, which lists the threads.

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_conversation`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_conversation`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_conversation
```

## Input

- `count` (integer, optional): Target number of messages to collect; the thread is scrolled back until this many are loaded or it reaches the beginning.
- `username` (string, optional): Handle of the person whose thread to read, with or without a leading @. Give this or conversationId.
- `conversationId` (string, optional): Conversation id as returned by the inbox script. Give this or username; it also addresses group threads, which have no single handle.

## Output

- `hasMore` (boolean, required): True when older messages were still loading beyond the ones returned.
- `messages` (array, required): Oldest first, in the order the thread renders them.
- `account_used` (string, required)
- `conversationId` (string, required)
- `nickname` (string | null, optional): Display name shown at the top of the thread.
- `username` (string | null, optional): Handle shown at the top of the thread, without the @.
- `participants` (array, optional)

## FAQ

### What does "Read a TikTok direct message conversation" do?

Read the messages in one of the signed-in account's direct message threads, addressed either by the other person's @username or by the conversation id the inbox script returns. Messages come back oldest to newest with the timestamp labels TikTok shows between them, and system notices in the thread (such as a message request being accepted) are marked as notices rather than passed off as messages. Opening a thread marks it as read, which is what the site does too. Pairs with the inbox script, which lists the threads.

### How do I automatically read a TikTok direct message conversation on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_conversation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_conversation

### Is there a tiktok.com API to read a TikTok direct message conversation?

You do not need one. "Read a TikTok direct message conversation" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Optional: count, username, conversationId.

### What does it return?

It returns hasMore, messages, nickname, username, account_used, participants, conversationId.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_conversation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_conversation

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_conversation
