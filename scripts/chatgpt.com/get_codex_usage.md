# Get ChatGPT Codex usage limits

Automatically get ChatGPT Codex usage limits on chatgpt.com. Read the Codex usage limits of the ChatGPT account open in this browser, as ChatGPT loads them for its Codex usage panel: the plan, whether Codex use is allowed right now and whether a limit is reached, and each usage window (on paid plans usually the 5-hour and the weekly window; on Free a single 30-day window) with its percent used, its length in seconds and its reset time (ISO), plus the code-review limit, any extra per-feature limits, and the credits state. ChatGPT chats have no usage meter of their own; these are the Codex limits that come with the ChatGPT plan. Read-only. A signed-out browser fails with an error that says to sign in; a refused or rate-limited usage request fails within seconds with the HTTP status.

- Site: chatgpt.com
- Address: `reduck/chatgpt.com/get_codex_usage`
- Updated: 2026-10-21 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chatgpt.com/get_codex_usage`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/get_codex_usage
```

## Input

It takes no input.

## Output

- `plan` (string | null, required)
- `email` (string | null, required)
- `readAt` (string, required)
- `allowed` (boolean | null, required)
- `credits` (object | null, required)
- `windows` (array, required)
- `accountId` (string | null, required)
- `limitReached` (boolean | null, required)
- `additionalLimits` (array, required)
- `limitReachedType` (string | null, required)
- `codeReviewWindows` (array, required)

## FAQ

### What does "Get ChatGPT Codex usage limits" do?

Read the Codex usage limits of the ChatGPT account open in this browser, as ChatGPT loads them for its Codex usage panel: the plan, whether Codex use is allowed right now and whether a limit is reached, and each usage window (on paid plans usually the 5-hour and the weekly window; on Free a single 30-day window) with its percent used, its length in seconds and its reset time (ISO), plus the code-review limit, any extra per-feature limits, and the credits state. ChatGPT chats have no usage meter of their own; these are the Codex limits that come with the ChatGPT plan. Read-only. A signed-out browser fails with an error that says to sign in; a refused or rate-limited usage request fails within seconds with the HTTP status.

### How do I automatically get ChatGPT Codex usage limits on chatgpt.com?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/get_codex_usage, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/get_codex_usage

### Is there a chatgpt.com API to get ChatGPT Codex usage limits?

You do not need one. "Get ChatGPT Codex usage limits" drives the real chatgpt.com pages in a browser, so it works whether or not chatgpt.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns plan, email, readAt, allowed, credits, windows, accountId, limitReached, additionalLimits, limitReachedType, codeReviewWindows.

### Do I need to be logged in to chatgpt.com?

Yes. It acts as you on chatgpt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the chatgpt.com cookies saved by the Reduck extension.

### Does it change anything on chatgpt.com, or only read data?

It only reads. It looks things up on chatgpt.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/get_codex_usage, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/get_codex_usage

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chatgpt.com/get_codex_usage
