# Get ChatGPT mode (Chat or Work)

Automatically get ChatGPT mode (Chat or Work) on chatgpt.com. Report whether ChatGPT answers new chats in Chat or Work mode in this browser, as the Chat/Work switch at the top of the home page shows it. The choice belongs to the browser, not the account, and a Chat choice lasts about four hours before ChatGPT falls back to Work, so check it before asking questions that need Chat. Requires a signed-in session; a signed-out browser fails with an error that says so. Use set_mode to change it.

- Site: chatgpt.com
- Address: `reduck/chatgpt.com/get_mode`
- Updated: 2026-10-22 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chatgpt.com/get_mode`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/get_mode
```

## Input

It takes no input.

## Output

- `mode` (string, required): The mode new chats open in.

## FAQ

### What does "Get ChatGPT mode (Chat or Work)" do?

Report whether ChatGPT answers new chats in Chat or Work mode in this browser, as the Chat/Work switch at the top of the home page shows it. The choice belongs to the browser, not the account, and a Chat choice lasts about four hours before ChatGPT falls back to Work, so check it before asking questions that need Chat. Requires a signed-in session; a signed-out browser fails with an error that says so. Use set_mode to change it.

### How do I automatically get ChatGPT mode (Chat or Work) on chatgpt.com?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/get_mode, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/get_mode

### Is there a chatgpt.com API to get ChatGPT mode (Chat or Work)?

You do not need one. "Get ChatGPT mode (Chat or Work)" drives the real chatgpt.com pages in a browser, so it works whether or not chatgpt.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns mode.

### Do I need to be logged in to chatgpt.com?

Yes. It acts as you on chatgpt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the chatgpt.com cookies saved by the Reduck extension.

### Does it change anything on chatgpt.com, or only read data?

It only reads. It looks things up on chatgpt.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/get_mode, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/get_mode

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chatgpt.com/get_mode
