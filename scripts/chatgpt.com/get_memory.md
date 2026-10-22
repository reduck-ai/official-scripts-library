# Get ChatGPT memory setting

Automatically get ChatGPT memory setting on chatgpt.com. Report whether memory is turned on for the signed-in ChatGPT account: the "Enable memory" switch in Settings > Personalization, which lets ChatGPT use saved memories and past chats to personalize its answers. Requires a signed-in session; a signed-out browser fails with an error that says so. Use set_memory to change it.

- Site: chatgpt.com
- Address: `reduck/chatgpt.com/get_memory`
- Updated: 2026-10-21 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chatgpt.com/get_memory`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/get_memory
```

## Input

It takes no input.

## Output

- `enabled` (boolean, required): True when memory is on for this account.

## FAQ

### What does "Get ChatGPT memory setting" do?

Report whether memory is turned on for the signed-in ChatGPT account: the "Enable memory" switch in Settings > Personalization, which lets ChatGPT use saved memories and past chats to personalize its answers. Requires a signed-in session; a signed-out browser fails with an error that says so. Use set_memory to change it.

### How do I automatically get ChatGPT memory setting on chatgpt.com?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/get_memory, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/get_memory

### Is there a chatgpt.com API to get ChatGPT memory setting?

You do not need one. "Get ChatGPT memory setting" drives the real chatgpt.com pages in a browser, so it works whether or not chatgpt.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns enabled.

### Do I need to be logged in to chatgpt.com?

Yes. It acts as you on chatgpt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the chatgpt.com cookies saved by the Reduck extension.

### Does it change anything on chatgpt.com, or only read data?

It only reads. It looks things up on chatgpt.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/get_memory, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/get_memory

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chatgpt.com/get_memory
