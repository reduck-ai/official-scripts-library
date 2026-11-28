# Search Muse memory (muse.ai)

Automatically search Muse memory (muse.ai) on muse.ai. Search the memory of the signed-in Muse account (Meta's personal agent at muse.ai) with Muse's own memory search, the one Muse uses to recall facts about you: its long-term memory file MEMORY.md and its daily notes (memory/YYYY-MM-DD.md). Returns the passages that match, best first: each with its text, the file and lines it is in, the kind of memory it is (memory_md for MEMORY.md, daily for a daily note), its relevance scores, and Muse's status and confidence for it. The search matches by meaning and by words, and returns only the passages it finds relevant: up to top_k (10 by default), and fewer, or none, when fewer are relevant. Muse updates its search index on its own schedule, and nothing tells when it has caught up: a fact Muse just saved was found after 2 minutes once, and still not after 20 minutes other times. To check a fact Muse just saved, read MEMORY.md with muse.ai/read_memory instead. Pass a hit's path to muse.ai/read_memory to read the whole file. Run Muse scripts one at a time: Muse lets only a few browser tabs hold an account's connection. Requires a signed-in session: a signed-out browser fails at once with an error that says so.

- Site: muse.ai
- Address: `reduck/muse.ai/search_memory`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/muse.ai/search_memory`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/muse.ai/search_memory
```

## Input

- `query` (string, required): What to look for, in words or as a question. It must hold at least one character that is not a space.
- `top_k` (integer, optional): The most passages to return. Muse returns 10 when it is omitted.

## Output

- `hits` (array, required): The passages that match, best first. Empty when nothing is relevant.

## FAQ

### What does "Search Muse memory (muse.ai)" do?

Search the memory of the signed-in Muse account (Meta's personal agent at muse.ai) with Muse's own memory search, the one Muse uses to recall facts about you: its long-term memory file MEMORY.md and its daily notes (memory/YYYY-MM-DD.md). Returns the passages that match, best first: each with its text, the file and lines it is in, the kind of memory it is (memory_md for MEMORY.md, daily for a daily note), its relevance scores, and Muse's status and confidence for it. The search matches by meaning and by words, and returns only the passages it finds relevant: up to top_k (10 by default), and fewer, or none, when fewer are relevant. Muse updates its search index on its own schedule, and nothing tells when it has caught up: a fact Muse just saved was found after 2 minutes once, and still not after 20 minutes other times. To check a fact Muse just saved, read MEMORY.md with muse.ai/read_memory instead. Pass a hit's path to muse.ai/read_memory to read the whole file. Run Muse scripts one at a time: Muse lets only a few browser tabs hold an account's connection. Requires a signed-in session: a signed-out browser fails at once with an error that says so.

### How do I automatically search Muse memory (muse.ai) on muse.ai?

Ask an AI agent connected to Reduck to run reduck/muse.ai/search_memory, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/search_memory

### Is there a muse.ai API to search Muse memory (muse.ai)?

You do not need one. "Search Muse memory (muse.ai)" drives the real muse.ai pages in a browser, so it works whether or not muse.ai offers an API for this.

### What information do I need to provide?

Required: query. Optional: top_k.

### What does it return?

It returns hits.

### Do I need to be logged in to muse.ai?

Yes. It acts as you on muse.ai: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for muse.ai.

### Does it change anything on muse.ai, or only read data?

It only reads. It looks things up on muse.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/muse.ai/search_memory, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/search_memory

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/muse.ai/search_memory
