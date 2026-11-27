# Read a Muse chat (muse.ai)

Automatically read a Muse chat (muse.ai) on muse.ai. Read one chat of the signed-in Muse account (Meta's personal agent at muse.ai) from its first message to its last: every message of the user and of Muse, and every card Muse showed in it (a browser task, shopping results, choices), oldest first, each with its text as markdown, its time, its status and the web pages Muse attached as sources. Long chats are read page by page to their start, so the chat comes back whole. Get a chat's id from muse.ai/list_chats, or the threadId that muse.ai/ask returns; it also reads the result Muse posts later in a chat that ask left pending. An id the account has no chat for fails with an error that says so. Requires a signed-in session: a signed-out browser fails at once with an error that says so.

- Site: muse.ai
- Address: `reduck/muse.ai/get_chat`
- Updated: 2026-11-26 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/muse.ai/get_chat`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/muse.ai/get_chat
```

## Input

- `chat_id` (string, required): The chat's id: an id from muse.ai/list_chats, or the threadId of muse.ai/ask.

## Output

- `url` (string, required): Where the chat opens on muse.ai: https://muse.ai/ for the main chat, https://muse.ai/thread/<id> for a side chat.
- `chat` (object, required): The chat as Muse lists it (the same fields as an item of muse.ai/list_chats).
- `messages` (array, required): Everything in the chat, oldest first, from its first message.

## FAQ

### What does "Read a Muse chat (muse.ai)" do?

Read one chat of the signed-in Muse account (Meta's personal agent at muse.ai) from its first message to its last: every message of the user and of Muse, and every card Muse showed in it (a browser task, shopping results, choices), oldest first, each with its text as markdown, its time, its status and the web pages Muse attached as sources. Long chats are read page by page to their start, so the chat comes back whole. Get a chat's id from muse.ai/list_chats, or the threadId that muse.ai/ask returns; it also reads the result Muse posts later in a chat that ask left pending. An id the account has no chat for fails with an error that says so. Requires a signed-in session: a signed-out browser fails at once with an error that says so.

### How do I automatically read a Muse chat (muse.ai) on muse.ai?

Ask an AI agent connected to Reduck to run reduck/muse.ai/get_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/get_chat

### Is there a muse.ai API to read a Muse chat (muse.ai)?

You do not need one. "Read a Muse chat (muse.ai)" drives the real muse.ai pages in a browser, so it works whether or not muse.ai offers an API for this.

### What information do I need to provide?

Required: chat_id.

### What does it return?

It returns url, chat, messages.

### Do I need to be logged in to muse.ai?

Yes. It acts as you on muse.ai: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for muse.ai.

### Does it change anything on muse.ai, or only read data?

It only reads. It looks things up on muse.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/muse.ai/get_chat, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/get_chat

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/muse.ai/get_chat
