# Get LinkedIn message thread

Automatically get LinkedIn message thread on linkedin.com. Read a classic LinkedIn messaging conversation (NOT Sales Navigator) by its thread URL from list_inbox. Returns the participants and messages (from, fromSelf, text, time, subject) in chronological order. Returns the most recent page only.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_thread`
- Updated: 2026-09-11 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_thread`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_thread
```

## Input

- `threadUrl` (string, required): A LinkedIn /messaging/thread/<id>/ URL, as returned by linkedin.com/list_inbox.

## FAQ

### What does "Get LinkedIn message thread" do?

Read a classic LinkedIn messaging conversation (NOT Sales Navigator) by its thread URL from list_inbox. Returns the participants and messages (from, fromSelf, text, time, subject) in chronological order. Returns the most recent page only.

### How do I automatically get LinkedIn message thread on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_thread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_thread

### Is there a linkedin.com API to get LinkedIn message thread?

You do not need one. "Get LinkedIn message thread" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: threadUrl.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_thread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_thread

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_thread
