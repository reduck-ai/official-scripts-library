# Edit sent message

Automatically edit sent message on linkedin.com. Edit a message you already sent in a classic LinkedIn messaging thread (NOT Sales Navigator), by thread URL from list_inbox. Edits your most recent message by default, or the most recent one containing `match`. LinkedIn only allows editing for ~60 minutes after sending — past that returns not_editable; the recipient sees an "(Edited)" tag. Only messages loaded in the thread's most recent page are searchable. Returns status (edited/not_found/not_editable), oldText and newText.

- Site: linkedin.com
- Address: `reduck/linkedin.com/edit_message`
- Updated: 2026-09-08 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/edit_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/edit_message
```

## Input

- `newText` (string, required): The replacement text for the message
- `threadUrl` (string, required): URL of the conversation thread, e.g. https://www.linkedin.com/messaging/thread/<id>/ (from list_inbox)
- `match` (string, optional): Optional substring of the current message text, used to pick which of your own messages to edit. Defaults to your most recent message in the thread. If several match, the most recent one wins.

## Output

- `status` (string, required): edited = saved; not_found = no own message (matching `match`) in the loaded thread; not_editable = LinkedIn's ~60min edit window has passed (no Edit item in the message menu)
- `newText` (string | null, required): The text that was saved (null unless status=edited)
- `oldText` (string | null, required): The message text before the edit (null when not_found)
- `threadUrl` (string, required)

## FAQ

### What does "Edit sent message" do?

Edit a message you already sent in a classic LinkedIn messaging thread (NOT Sales Navigator), by thread URL from list_inbox. Edits your most recent message by default, or the most recent one containing `match`. LinkedIn only allows editing for ~60 minutes after sending — past that returns not_editable; the recipient sees an "(Edited)" tag. Only messages loaded in the thread's most recent page are searchable. Returns status (edited/not_found/not_editable), oldText and newText.

### How do I automatically edit sent message on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/edit_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/edit_message

### Is there a linkedin.com API to edit sent message?

You do not need one. "Edit sent message" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: threadUrl, newText. Optional: match.

### What does it return?

It returns status, newText, oldText, threadUrl.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/edit_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/edit_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/edit_message
