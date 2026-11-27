# Search Muse chats (muse.ai)

Automatically search Muse chats (muse.ai) on muse.ai. Search the messages of the signed-in Muse account (Meta's personal agent at muse.ai) with Muse's own search, and return one page of the messages that match, newest first: each message (from the user or from Muse) with its text as markdown, its time and its sources, the chat it is in, and the extract Muse shows for the match. All chats are searched, archived chats included, or only the main chat with main_chat_only: true. A page holds up to 100 messages. When has_more is true, run the same search again with before set to next_before to get the next page. A search that matches nothing returns an empty list. Pass a hit's chat id to muse.ai/get_chat to read the whole chat, or to muse.ai/send_message to continue it. Requires a signed-in session: a signed-out browser fails at once with an error that says so.

- Site: muse.ai
- Address: `reduck/muse.ai/search_chats`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/muse.ai/search_chats`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/muse.ai/search_chats
```

## Input

- `query` (string, required): The words to search for, as typed in Muse's search box. It must hold at least one character that is not a space.
- `before` (integer, optional): The next_before of the previous page, to get the page after it. Omit it for the first page.
- `main_chat_only` (boolean, optional): true searches only the account's main chat. false (the default) searches every chat.

## Output

- `hits` (array, required): The messages of this page that match, newest first. Empty when nothing matches.
- `has_more` (boolean, required): True when older messages also match: pass next_before as before to get them.
- `next_before` (integer | null, required): The value of before for the next page. Null when has_more is false.

## FAQ

### What does "Search Muse chats (muse.ai)" do?

Search the messages of the signed-in Muse account (Meta's personal agent at muse.ai) with Muse's own search, and return one page of the messages that match, newest first: each message (from the user or from Muse) with its text as markdown, its time and its sources, the chat it is in, and the extract Muse shows for the match. All chats are searched, archived chats included, or only the main chat with main_chat_only: true. A page holds up to 100 messages. When has_more is true, run the same search again with before set to next_before to get the next page. A search that matches nothing returns an empty list. Pass a hit's chat id to muse.ai/get_chat to read the whole chat, or to muse.ai/send_message to continue it. Requires a signed-in session: a signed-out browser fails at once with an error that says so.

### How do I automatically search Muse chats (muse.ai) on muse.ai?

Ask an AI agent connected to Reduck to run reduck/muse.ai/search_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/search_chats

### Is there a muse.ai API to search Muse chats (muse.ai)?

You do not need one. "Search Muse chats (muse.ai)" drives the real muse.ai pages in a browser, so it works whether or not muse.ai offers an API for this.

### What information do I need to provide?

Required: query. Optional: before, main_chat_only.

### What does it return?

It returns hits, has_more, next_before.

### Do I need to be logged in to muse.ai?

Yes. It acts as you on muse.ai: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for muse.ai.

### Does it change anything on muse.ai, or only read data?

It only reads. It looks things up on muse.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/muse.ai/search_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/search_chats

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/muse.ai/search_chats
