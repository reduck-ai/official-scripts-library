# List Muse memory files (muse.ai)

Automatically list Muse memory files (muse.ai) on muse.ai. List every file of the memory of the signed-in Muse account (Meta's personal agent at muse.ai): its long-term memory MEMORY.md, each file under memory/ in every subfolder (the daily notes such as memory/2026-11-25.md, the memory banks memory/bank/world.md, opinions.md, experience.md, reflections.md, and the indexes of people, groups and shopping), and each file under dreams/, where Muse's nightly pass writes what it learned about the user (dreams/alignment/derived/ALIGNMENT_SYNTHESIS.md) and a diary per day. Each file comes with its path, its size and when Muse last changed it, in the order Muse lists them. Pass a path to muse.ai/read_memory to read the file, or search MEMORY.md and the daily notes with muse.ai/search_memory. Run Muse scripts one at a time: Muse lets only a few browser tabs hold an account's connection. Requires a signed-in session: a signed-out browser fails at once with an error that says so.

- Site: muse.ai
- Address: `reduck/muse.ai/list_memory`
- Updated: 2026-11-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/muse.ai/list_memory`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/muse.ai/list_memory
```

## Input

It takes no input.

## Output

- `files` (array, required): Every memory file, sorted by path. MEMORY.md is left out when the account has none.

## FAQ

### What does "List Muse memory files (muse.ai)" do?

List every file of the memory of the signed-in Muse account (Meta's personal agent at muse.ai): its long-term memory MEMORY.md, each file under memory/ in every subfolder (the daily notes such as memory/2026-11-25.md, the memory banks memory/bank/world.md, opinions.md, experience.md, reflections.md, and the indexes of people, groups and shopping), and each file under dreams/, where Muse's nightly pass writes what it learned about the user (dreams/alignment/derived/ALIGNMENT_SYNTHESIS.md) and a diary per day. Each file comes with its path, its size and when Muse last changed it, in the order Muse lists them. Pass a path to muse.ai/read_memory to read the file, or search MEMORY.md and the daily notes with muse.ai/search_memory. Run Muse scripts one at a time: Muse lets only a few browser tabs hold an account's connection. Requires a signed-in session: a signed-out browser fails at once with an error that says so.

### How do I automatically list Muse memory files (muse.ai) on muse.ai?

Ask an AI agent connected to Reduck to run reduck/muse.ai/list_memory, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/list_memory

### Is there a muse.ai API to list Muse memory files (muse.ai)?

You do not need one. "List Muse memory files (muse.ai)" drives the real muse.ai pages in a browser, so it works whether or not muse.ai offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns files.

### Do I need to be logged in to muse.ai?

Yes. It acts as you on muse.ai: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for muse.ai.

### Does it change anything on muse.ai, or only read data?

It only reads. It looks things up on muse.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/muse.ai/list_memory, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/list_memory

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/muse.ai/list_memory
