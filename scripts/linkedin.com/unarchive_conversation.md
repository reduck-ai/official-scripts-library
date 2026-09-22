# unarchive_conversation

Move a LinkedIn classic-messaging conversation (not Sales Navigator) out of Archived and back into the main inbox, by its thread url from list_inbox. Returns whether it was unarchived, and already_active if the conversation was not archived to begin with.

- Site: linkedin.com
- Address: `reduck/linkedin.com/unarchive_conversation`
- Updated: 2026-09-03 (v27)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/unarchive_conversation`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/unarchive_conversation
```

## Input

- `threadUrl` (string, required): Full thread url, e.g. https://www.linkedin.com/messaging/thread/<threadId>/, as returned by linkedin.com/list_inbox.

## Output

- `threadId` (string, required)
- `unarchived` (boolean, required)
- `already_active` (boolean, required)

## FAQ

### What does "unarchive_conversation" do?

Move a LinkedIn classic-messaging conversation (not Sales Navigator) out of Archived and back into the main inbox, by its thread url from list_inbox. Returns whether it was unarchived, and already_active if the conversation was not archived to begin with.

### What information do I need to provide?

Required: threadUrl.

### What does it return?

It returns threadId, unarchived, already_active.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/unarchive_conversation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/unarchive_conversation

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/unarchive_conversation
