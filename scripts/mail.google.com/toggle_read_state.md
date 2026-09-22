# Toggle Gmail thread read state

Automatically toggle Gmail thread read state on mail.google.com. Mark a Gmail thread as read or unread by its hex threadId. Pass read:true to mark as read (default), read:false to mark as unread. Returns the final read state, threadId, the All Mail page it was found on, and already_read/already_unread flags. Acts from the All Mail list, scanning the first 4 pages (~200 newest threads). A thread already in the requested state is left alone and comes back with already_read:true or already_unread:true, so repeating the call is safe. Waits for Gmail to persist the change rather than returning on optimistic row restyling.

- Site: mail.google.com
- Address: `reduck/mail.google.com/toggle_read_state`
- Updated: 2026-09-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/toggle_read_state`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/toggle_read_state
```

## Input

- `threadId` (string, required): Hex legacy thread id (as returned by search_emails).
- `read` (boolean, optional): true to mark as read (default), false to mark as unread.
- `account` (string, optional): Google account email to act as (authuser=). Without it Gmail picks u/0, nondeterministic in a multi-account browser jar.

## Output

- `page` (integer, required): Which All Mail page the thread was found on (1-based).
- `threadId` (string, required)
- `read` (boolean, optional): The final read state: true if thread is now read.
- `unread` (boolean, optional): The final unread state: true if thread is now unread.
- `already_read` (boolean, optional): true = the thread was already read; nothing was clicked.
- `already_unread` (boolean, optional): true = the thread was already unread; nothing was clicked.

## FAQ

### What does "Toggle Gmail thread read state" do?

Mark a Gmail thread as read or unread by its hex threadId. Pass read:true to mark as read (default), read:false to mark as unread. Returns the final read state, threadId, the All Mail page it was found on, and already_read/already_unread flags. Acts from the All Mail list, scanning the first 4 pages (~200 newest threads). A thread already in the requested state is left alone and comes back with already_read:true or already_unread:true, so repeating the call is safe. Waits for Gmail to persist the change rather than returning on optimistic row restyling.

### How do I automatically toggle Gmail thread read state on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/toggle_read_state, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/toggle_read_state

### Is there a mail.google.com API to toggle Gmail thread read state?

You do not need one. "Toggle Gmail thread read state" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: threadId. Optional: read, account.

### What does it return?

It returns page, read, unread, threadId, already_read, already_unread.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/toggle_read_state, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/toggle_read_state

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/toggle_read_state
