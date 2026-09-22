# Get Claude Code session

Automatically get Claude Code session on claude.ai. Full transcript of one Claude Code web session by id, oldest→newest. The transcript is virtualized — only the messages near the viewport exist in the DOM — so this walks it from the top and stops on the count the list itself declares (aria-setsize), rather than guessing when it has seen everything; a read it cannot complete throws instead of returning a partial transcript that would look whole. Each message carries its own id, who sent it (human, assistant, or neither for a system card like "Context cleared"), and the readable text of what the page shows for that turn — prose plus the tool cards' own summaries, in reading order. No timestamp: the page only holds an absolute one in a per-message hover tooltip.

- Site: claude.ai
- Address: `reduck/claude.ai/get_code_session`
- Updated: 2026-09-15 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/get_code_session`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/get_code_session
```

## Input

- `session_id` (string, required): The session id as returned by list_code_sessions (also the /code/<id> URL segment), e.g. "session_01ESfPiAadbkS23eBAtynZTL".

## Output

- `id` (string, required)
- `title` (string | null, required): The session's title as shown in the title bar.
- `messages` (array, required)
- `message_count` (integer, required): How many messages the transcript declares (aria-setsize). Always equals messages.length: a read that could not complete throws rather than returning.

## FAQ

### What does "Get Claude Code session" do?

Full transcript of one Claude Code web session by id, oldest→newest. The transcript is virtualized — only the messages near the viewport exist in the DOM — so this walks it from the top and stops on the count the list itself declares (aria-setsize), rather than guessing when it has seen everything; a read it cannot complete throws instead of returning a partial transcript that would look whole. Each message carries its own id, who sent it (human, assistant, or neither for a system card like "Context cleared"), and the readable text of what the page shows for that turn — prose plus the tool cards' own summaries, in reading order. No timestamp: the page only holds an absolute one in a per-message hover tooltip.

### How do I automatically get Claude Code session on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/get_code_session, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/get_code_session

### Is there a claude.ai API to get Claude Code session?

You do not need one. "Get Claude Code session" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Required: session_id.

### What does it return?

It returns id, title, messages, message_count.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It only reads. It looks things up on claude.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/get_code_session, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/get_code_session

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/get_code_session
