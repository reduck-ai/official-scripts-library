# Send a Gmail draft

Automatically send a Gmail draft on mail.google.com. Send an existing Gmail draft by its id from mail.google.com/list_drafts: a new message, or a reply saved inside a conversation. Delivers a real message that cannot be undone. Returns the recipients, subject and conversation id. Fails with nothing sent for an unknown id or a draft with no recipient. Sending a reply opens its conversation, which marks it as read. Pass account (an email) when several Google accounts share the browser.

- Site: mail.google.com
- Address: `reduck/mail.google.com/send_draft`
- Updated: 2026-11-10 (v12)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/send_draft`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/send_draft
```

## Input

- `draftId` (string, required): The draft's current id, from mail.google.com/list_drafts: a new message or a reply saved inside a conversation. Gmail replaces a draft's id every time it is saved, so use a freshly listed one.
- `account` (string, optional): Google account email whose draft this is. Without it Gmail opens the first signed-in account (u/0), which may not be the one holding the draft when several accounts share the browser.

## Output

- `sent` (boolean, required): True when the message was actually sent. Always true on success: the script fails instead of returning false.
- `subject` (string | null, required): Subject of the message that was sent. Empty when the draft had no subject.
- `threadId` (string, required): Conversation id, unchanged by sending, so the sent message can be located afterwards.
- `account_used` (string, required): The Gmail account the message was sent from, read from the session.
- `verified_on_page` (boolean, required): True when Gmail confirmed the send or the message showed in Sent.
- `recipientsDisplay` (string, required): The recipients as the compose window lists them (display names).
- `sender` (string | null, optional): The address the message was sent from (same as account_used).
- `isReply` (boolean, optional): True when the draft was a reply saved inside a conversation, false for a new message.
- `attempts` (integer, optional): How many Send clicks it took before Gmail accepted.
- `leftDrafts` (boolean, optional): Whether the draft had left Drafts by the time this was checked.
- `recipients` (array, optional): The To addresses as the compose window holds them.
- `foundInSent` (boolean, optional): Whether the message was found in Sent afterwards.
- `previousDraftId` (string, optional): The draft id that was sent and no longer exists as a draft.
- `accepted_by_server` (boolean, optional): True when Gmail confirmed it accepted the send.

## FAQ

### What does "Send a Gmail draft" do?

Send an existing Gmail draft by its id from mail.google.com/list_drafts: a new message, or a reply saved inside a conversation. Delivers a real message that cannot be undone. Returns the recipients, subject and conversation id. Fails with nothing sent for an unknown id or a draft with no recipient. Sending a reply opens its conversation, which marks it as read. Pass account (an email) when several Google accounts share the browser.

### How do I automatically send a Gmail draft on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/send_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/send_draft

### Is there a mail.google.com API to send a Gmail draft?

You do not need one. "Send a Gmail draft" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: draftId. Optional: account.

### What does it return?

It returns sent, sender, isReply, subject, attempts, threadId, leftDrafts, recipients, foundInSent, account_used, previousDraftId, verified_on_page, recipientsDisplay, accepted_by_server.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/send_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/send_draft

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/send_draft
