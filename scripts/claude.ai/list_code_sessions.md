# List Claude Code sessions

Automatically list Claude Code sessions on claude.ai. List your Claude Code web sessions (the Recents list in the /code sidebar), newest first. Each entry carries the session id used by get_code_session, its full title, and the live status the sidebar dot reports (e.g. Running, Needs input) when it shows one. An account with no sessions yet returns an empty list. Claude Code sessions are not part of /recents ("Chats and tasks") — that page's Cowork filter is a different feature — so this sidebar list is the surface that has them.

- Site: claude.ai
- Address: `reduck/claude.ai/list_code_sessions`
- Updated: 2026-08-20 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/list_code_sessions`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_code_sessions
```

## Input

- `limit` (integer, optional): Max sessions to return. Omit for every session the sidebar holds.

## FAQ

### What does "List Claude Code sessions" do?

List your Claude Code web sessions (the Recents list in the /code sidebar), newest first. Each entry carries the session id used by get_code_session, its full title, and the live status the sidebar dot reports (e.g. Running, Needs input) when it shows one. An account with no sessions yet returns an empty list. Claude Code sessions are not part of /recents ("Chats and tasks") — that page's Cowork filter is a different feature — so this sidebar list is the surface that has them.

### How do I automatically list Claude Code sessions on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/list_code_sessions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_code_sessions

### Is there a claude.ai API to list Claude Code sessions?

You do not need one. "List Claude Code sessions" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Optional: limit.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It only reads. It looks things up on claude.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/list_code_sessions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_code_sessions

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/list_code_sessions
