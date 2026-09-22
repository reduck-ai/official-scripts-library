# Mark an Outlook.com email read or unread

Automatically mark an Outlook.com email read or unread on outlook.live.com. Mark one Outlook.com (outlook.live.com) message as read or unread by its id (from list_emails), confirming the state actually changed.

- Site: outlook.live.com
- Address: `reduck/outlook.live.com/set_read_state`
- Updated: 2026-09-16 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/outlook.live.com/set_read_state`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/set_read_state
```

## Input

- `id` (string, required): Message id from list_emails (the row's id attribute).
- `read` (boolean, required): true marks the message read, false marks it unread.
- `folder` (string, optional): Folder the message is in, as shown in your folder list.

## Output

- `id` (string, required)
- `read` (boolean, required): The state requested.
- `folder` (string, required)
- `changed` (boolean, required): True when the row's own rendering confirms it flipped. False when it was already in the requested state.
- `wasAlready` (boolean, optional): True when the message was already in the requested state, so nothing was done.
- `unreadCountAfter` (number | null, optional)
- `unreadCountBefore` (number | null, optional)

## FAQ

### What does "Mark an Outlook.com email read or unread" do?

Mark one Outlook.com (outlook.live.com) message as read or unread by its id (from list_emails), confirming the state actually changed.

### How do I automatically mark an Outlook.com email read or unread on outlook.live.com?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/set_read_state, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/set_read_state

### Is there a outlook.live.com API to mark an Outlook.com email read or unread?

You do not need one. "Mark an Outlook.com email read or unread" drives the real outlook.live.com pages in a browser, so it works whether or not outlook.live.com offers an API for this.

### What information do I need to provide?

Required: id, read. Optional: folder.

### What does it return?

It returns id, read, folder, changed, wasAlready, unreadCountAfter, unreadCountBefore.

### Do I need to be logged in to outlook.live.com?

Yes. It acts as you on outlook.live.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the outlook.live.com cookies saved by the Reduck extension.

### Does it change anything on outlook.live.com, or only read data?

It makes changes on outlook.live.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/set_read_state, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/set_read_state

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/outlook.live.com/set_read_state
