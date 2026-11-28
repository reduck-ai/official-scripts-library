# Read what Muse did in a chat (muse.ai)

Automatically read what Muse did in a chat (muse.ai) on muse.ai. Read what Muse (Meta's personal agent at muse.ai) did to answer in one chat of the signed-in account, as its activity panel records it: each task Muse worked on, with every step in order (the main agent's tool calls and those of the browser agent it launched), each step's title, status, time and report, and the screenshots Muse's browser took during that step. Also the web searches Muse ran for the chat's replies, with their queries.

- Site: muse.ai
- Address: `reduck/muse.ai/get_activity`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/muse.ai/get_activity`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/muse.ai/get_activity
```

## Input

- `chat_id` (string, required): The chat's id: an id from muse.ai/list_chats, or the threadId of muse.ai/ask.

## Output

- `url` (string, required): Where the chat opens on muse.ai.
- `tasks` (array, required): The tasks Muse worked on for this chat, as its activity panel lists them, newest first. A chat can have several: Muse can come back to a chat on its own later.
- `chat_id` (string, required)
- `searches` (array, required): The web searches Muse ran for this chat's replies, as its activity list gives them: details holds the query (or items, a list of queries) and the tool.

## FAQ

### What does "Read what Muse did in a chat (muse.ai)" do?

Read what Muse (Meta's personal agent at muse.ai) did to answer in one chat of the signed-in account, as its activity panel records it: each task Muse worked on, with every step in order (the main agent's tool calls and those of the browser agent it launched), each step's title, status, time and report, and the screenshots Muse's browser took during that step. Also the web searches Muse ran for the chat's replies, with their queries.

### How do I automatically read what Muse did in a chat (muse.ai) on muse.ai?

Ask an AI agent connected to Reduck to run reduck/muse.ai/get_activity, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/get_activity

### Is there a muse.ai API to read what Muse did in a chat (muse.ai)?

You do not need one. "Read what Muse did in a chat (muse.ai)" drives the real muse.ai pages in a browser, so it works whether or not muse.ai offers an API for this.

### What information do I need to provide?

Required: chat_id.

### What does it return?

It returns url, tasks, chat_id, searches.

### Do I need to be logged in to muse.ai?

Yes. It acts as you on muse.ai: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for muse.ai.

### Does it change anything on muse.ai, or only read data?

It only reads. It looks things up on muse.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/muse.ai/get_activity, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/get_activity

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/muse.ai/get_activity
