# Get Claude Code session

Automatically get Claude Code session on claude.ai. Read the transcript of one of your Claude Code sessions on claude.ai, one batch at a time, newest batch first. Each batch lists your prompts and Claude's replies in reading order, with the tools Claude called by name; tool results, thinking and system events are left out. Pass the returned nextCursor with the same session_id to get the older batch; it is null once the batch reaches the start of the session. A session the account does not have fails with a message to check the id with claude.ai/list_code_sessions.

- Site: claude.ai
- Address: `reduck/claude.ai/get_code_session`
- Updated: 2026-10-28 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/get_code_session`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/get_code_session
```

## Input

- `session_id` (string, required): The session id from the session URL or from claude.ai/list_code_sessions, e.g. session_01PsJP8rAX1Ab7K36GbqH9kJ.
- `cursor` (string, optional): nextCursor from a previous run on the same session, to get the older batch. Omit for the newest batch.

## Output

- `id` (string, required)
- `title` (string | null, required): The session's title. Null when the session has none.
- `messages` (array, required): This batch's messages in reading order, oldest first. A batch can be empty when it holds only tool results or system events.
- `nextCursor` (string | null, required): Pass as cursor (with the same session_id) for the older batch of messages. Null when this batch reaches the start of the session.

## FAQ

### What does "Get Claude Code session" do?

Read the transcript of one of your Claude Code sessions on claude.ai, one batch at a time, newest batch first. Each batch lists your prompts and Claude's replies in reading order, with the tools Claude called by name; tool results, thinking and system events are left out. Pass the returned nextCursor with the same session_id to get the older batch; it is null once the batch reaches the start of the session. A session the account does not have fails with a message to check the id with claude.ai/list_code_sessions.

### How do I automatically get Claude Code session on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/get_code_session, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/get_code_session

### Is there a claude.ai API to get Claude Code session?

You do not need one. "Get Claude Code session" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Required: session_id. Optional: cursor.

### What does it return?

It returns id, title, messages, nextCursor.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It only reads. It looks things up on claude.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/get_code_session, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/get_code_session

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/get_code_session
