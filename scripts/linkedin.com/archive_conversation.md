# Archive/restore LinkedIn conversation

Archive or restore a classic LinkedIn messaging conversation (NOT Sales Navigator), by thread URL from list_inbox. LinkedIn exposes this as a single toggle: archiving a conversation removes it from the main inbox, and running this again on an already-archived conversation restores it back to the inbox. Returns which direction was applied (archived/restored).

- Site: linkedin.com
- Address: `reduck/linkedin.com/archive_conversation`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/archive_conversation`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/archive_conversation
```

## Input

- `threadUrl` (string, required): URL of the conversation thread, e.g. https://www.linkedin.com/messaging/thread/<id>/ (from list_inbox)

## Output

- `status` (string, required): archived = the conversation was moved out of the inbox; restored = an already-archived conversation was moved back into the inbox
- `threadUrl` (string, required)

## FAQ

### What does "Archive/restore LinkedIn conversation" do?

Archive or restore a classic LinkedIn messaging conversation (NOT Sales Navigator), by thread URL from list_inbox. LinkedIn exposes this as a single toggle: archiving a conversation removes it from the main inbox, and running this again on an already-archived conversation restores it back to the inbox. Returns which direction was applied (archived/restored).

### What information do I need to provide?

Required: threadUrl.

### What does it return?

It returns status, threadUrl.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/archive_conversation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/archive_conversation

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/archive_conversation
