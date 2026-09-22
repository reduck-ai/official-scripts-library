# Delete sent LinkedIn message

Automatically delete sent LinkedIn message on linkedin.com. Permanently delete one of the logged-in member's own sent messages in a classic LinkedIn messaging thread (NOT Sales Navigator), by thread URL from list_inbox. Deletes your most recent message by default, or the most recent one containing `match`. The message is deleted for all participants and replaced with a "This message has been deleted" placeholder. Returns status (deleted/not_found) and the deleted text.

- Site: linkedin.com
- Address: `reduck/linkedin.com/delete_message`
- Updated: 2026-09-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/delete_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/delete_message
```

## Input

- `threadUrl` (string, required): URL of the conversation thread, e.g. https://www.linkedin.com/messaging/thread/<id>/ (from list_inbox)
- `match` (string, optional): Optional substring of the message text to pick WHICH of your own messages to delete. Defaults to your most recent message in the thread. If several match, the most recent one wins.

## Output

- `status` (string, required): deleted = removed; not_found = no own (non-already-deleted) message matching `match` in the loaded thread; not_deletable = a matching message was found but LinkedIn's per-message menu doesn't offer Delete for it (observed on older messages -- deletion appears to have its own time window, separate from the ~60min edit window)
- `threadUrl` (string, required)
- `deletedText` (string | null, required): The message text that was deleted (null unless status=deleted)

## FAQ

### What does "Delete sent LinkedIn message" do?

Permanently delete one of the logged-in member's own sent messages in a classic LinkedIn messaging thread (NOT Sales Navigator), by thread URL from list_inbox. Deletes your most recent message by default, or the most recent one containing `match`. The message is deleted for all participants and replaced with a "This message has been deleted" placeholder. Returns status (deleted/not_found) and the deleted text.

### How do I automatically delete sent LinkedIn message on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/delete_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/delete_message

### Is there a linkedin.com API to delete sent LinkedIn message?

You do not need one. "Delete sent LinkedIn message" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: threadUrl. Optional: match.

### What does it return?

It returns status, threadUrl, deletedText.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/delete_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/delete_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/delete_message
