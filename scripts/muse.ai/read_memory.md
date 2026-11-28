# Read a Muse memory file (muse.ai)

Automatically read a Muse memory file (muse.ai) on muse.ai. Read one file of the memory of the signed-in Muse account (Meta's personal agent at muse.ai), whole: its long-term memory MEMORY.md, a daily note (memory/2026-11-25.md), or a memory bank or index under memory/ (memory/bank/world.md). Returns the file's markdown as Muse holds it, with its size and when Muse last changed it. A memory bank line ends with (src: <file>:<line>), the note it was taken from. Get a path from muse.ai/list_memory or from a hit of muse.ai/search_memory; the lines of a hit are lines of this text, counted from 1. Any other file of Muse's home folder can be read the same way (USER.md, SOUL.md). A path that names no file, or names a folder, fails with an error that says so. Requires a signed-in session: a signed-out browser fails at once with an error that says so.

- Site: muse.ai
- Address: `reduck/muse.ai/read_memory`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/muse.ai/read_memory`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/muse.ai/read_memory
```

## Input

- `path` (string, required): The file's path in Muse's home folder, as list_memory and search_memory give it: MEMORY.md, memory/2026-11-25.md. It does not start with a slash.

## Output

- `path` (string, required): The path read.
- `size` (integer, required): Its size in bytes.
- `text` (string, required): The whole file, as markdown.
- `modifiedAt` (string | null, required): When Muse last changed it, ISO 8601.

## FAQ

### What does "Read a Muse memory file (muse.ai)" do?

Read one file of the memory of the signed-in Muse account (Meta's personal agent at muse.ai), whole: its long-term memory MEMORY.md, a daily note (memory/2026-11-25.md), or a memory bank or index under memory/ (memory/bank/world.md). Returns the file's markdown as Muse holds it, with its size and when Muse last changed it. A memory bank line ends with (src: <file>:<line>), the note it was taken from. Get a path from muse.ai/list_memory or from a hit of muse.ai/search_memory; the lines of a hit are lines of this text, counted from 1. Any other file of Muse's home folder can be read the same way (USER.md, SOUL.md). A path that names no file, or names a folder, fails with an error that says so. Requires a signed-in session: a signed-out browser fails at once with an error that says so.

### How do I automatically read a Muse memory file (muse.ai) on muse.ai?

Ask an AI agent connected to Reduck to run reduck/muse.ai/read_memory, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/read_memory

### Is there a muse.ai API to read a Muse memory file (muse.ai)?

You do not need one. "Read a Muse memory file (muse.ai)" drives the real muse.ai pages in a browser, so it works whether or not muse.ai offers an API for this.

### What information do I need to provide?

Required: path.

### What does it return?

It returns path, size, text, modifiedAt.

### Do I need to be logged in to muse.ai?

Yes. It acts as you on muse.ai: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for muse.ai.

### Does it change anything on muse.ai, or only read data?

It only reads. It looks things up on muse.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/muse.ai/read_memory, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/read_memory

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/muse.ai/read_memory
