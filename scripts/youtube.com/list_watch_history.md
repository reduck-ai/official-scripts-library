# List YouTube watch history

Automatically list YouTube watch history on youtube.com. List the videos and Shorts in your YouTube watch history, newest first, as the history page shows them: one entry per video with its day heading, id, title, url, channel, view count, duration and how much of it was watched. Returns the first page of the history (about 200 entries) and a nextCursor when older entries exist. Returns an empty list when watch history is paused or cleared for the account.

- Site: youtube.com
- Address: `reduck/youtube.com/list_watch_history`
- Updated: 2026-09-17 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/youtube.com/list_watch_history`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/youtube.com/list_watch_history
```

## Input

It takes no input.

## Output

- `items` (array, required)
- `nextCursor` (string | null, required): Opaque token present when older history exists beyond this page. Informational: this script returns the first page only.

## FAQ

### What does "List YouTube watch history" do?

List the videos and Shorts in your YouTube watch history, newest first, as the history page shows them: one entry per video with its day heading, id, title, url, channel, view count, duration and how much of it was watched. Returns the first page of the history (about 200 entries) and a nextCursor when older entries exist. Returns an empty list when watch history is paused or cleared for the account.

### How do I automatically list YouTube watch history on youtube.com?

Ask an AI agent connected to Reduck to run reduck/youtube.com/list_watch_history, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/list_watch_history

### Is there a youtube.com API to list YouTube watch history?

You do not need one. "List YouTube watch history" drives the real youtube.com pages in a browser, so it works whether or not youtube.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns items, nextCursor.

### Do I need to be logged in to youtube.com?

Yes. It acts as you on youtube.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the youtube.com cookies saved by the Reduck extension.

### Does it change anything on youtube.com, or only read data?

It only reads. It looks things up on youtube.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/youtube.com/list_watch_history, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/youtube.com/list_watch_history

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/youtube.com/list_watch_history
