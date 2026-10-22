# Get Claude.ai memory settings

Automatically get Claude.ai memory settings on claude.ai. Report the two memory switches of the signed-in Claude.ai account, from Settings > Memory: `searchChats` (Claude may search and reference past chats) and `generateMemory` (Claude builds memory from your chats). Memory is fully off only when both are false. Reads the organisation the browser has open. Requires a signed-in session; a signed-out browser fails with an error that says so. Use set_memory to change them.

- Site: claude.ai
- Address: `reduck/claude.ai/get_memory`
- Updated: 2026-10-21 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/get_memory`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/get_memory
```

## Input

It takes no input.

## Output

- `searchChats` (boolean, required): True when Claude may search and reference past chats.
- `generateMemory` (boolean, required): True when Claude generates memory from your chats.

## FAQ

### What does "Get Claude.ai memory settings" do?

Report the two memory switches of the signed-in Claude.ai account, from Settings > Memory: `searchChats` (Claude may search and reference past chats) and `generateMemory` (Claude builds memory from your chats). Memory is fully off only when both are false. Reads the organisation the browser has open. Requires a signed-in session; a signed-out browser fails with an error that says so. Use set_memory to change them.

### How do I automatically get Claude.ai memory settings on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/get_memory, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/get_memory

### Is there a claude.ai API to get Claude.ai memory settings?

You do not need one. "Get Claude.ai memory settings" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns searchChats, generateMemory.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It only reads. It looks things up on claude.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/get_memory, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/get_memory

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/get_memory
