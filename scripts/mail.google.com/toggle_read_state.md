# Toggle Gmail thread read state

Automatically toggle Gmail thread read state on mail.google.com. Mark a Gmail thread as read or unread by its hex threadId, in the chosen Google account. Pass read:true to mark as read (default), read:false to mark as unread. Returns the final read and unread state, threadId, and already_read/already_unread when the thread was already in the requested state and was left alone, so repeating the call is safe. Success is reported only once Gmail has saved the change and a fresh read confirms it. An unknown or malformed id is refused without changing anything.

- Site: mail.google.com
- Address: `reduck/mail.google.com/toggle_read_state`
- Updated: 2026-10-21 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/toggle_read_state`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/toggle_read_state
```

## Input

- `threadId` (string, required): Hex legacy thread id (as returned by search_emails).
- `read` (boolean, optional): true to mark as read (default), false to mark as unread.
- `account` (string, optional): The Google account whose thread this is: its email address, or Gmail's account number in this browser (e.g. "2"). The run fails if that account is not signed in. Omit for the first signed-in account (u/0).

## Output

- `read` (boolean, required): The final read state: true if thread is now read.
- `unread` (boolean, required): The final unread state: true if thread is now unread.
- `threadId` (string, required)
- `already_read` (boolean, optional): true = the thread was already read; nothing was clicked.
- `already_unread` (boolean, optional): true = the thread was already unread; nothing was clicked.

## FAQ

### What does "Toggle Gmail thread read state" do?

Mark a Gmail thread as read or unread by its hex threadId, in the chosen Google account. Pass read:true to mark as read (default), read:false to mark as unread. Returns the final read and unread state, threadId, and already_read/already_unread when the thread was already in the requested state and was left alone, so repeating the call is safe. Success is reported only once Gmail has saved the change and a fresh read confirms it. An unknown or malformed id is refused without changing anything.

### How do I automatically toggle Gmail thread read state on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/toggle_read_state, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/toggle_read_state

### Is there a mail.google.com API to toggle Gmail thread read state?

You do not need one. "Toggle Gmail thread read state" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: threadId. Optional: read, account.

### What does it return?

It returns read, unread, threadId, already_read, already_unread.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/toggle_read_state, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/toggle_read_state

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/toggle_read_state
