# Send a Gmail draft

Automatically send a Gmail draft on mail.google.com. Send an existing Gmail draft, identified by the id the drafts listing gives you: a new message, or a reply saved inside a conversation. This delivers a real message and cannot be undone. The draft's recipients and subject are reported back with the send, and a draft with no recipient is refused rather than attempted. The call succeeds only once Gmail confirms the send; otherwise it fails and says whether anything may have gone out. The conversation id is returned and is the same before and after sending, so the message can be found again afterwards. Sending a reply opens its conversation, which marks it as read.

- Site: mail.google.com
- Address: `reduck/mail.google.com/send_draft`
- Updated: 2026-10-22 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/send_draft`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/send_draft
```

## Input

- `draftId` (string, required): The draft's current id, as returned by the drafts listing: a new message or a reply saved inside a conversation. Gmail replaces a draft's id every time it is saved, so use a freshly listed one.
- `account` (string, optional): Google account email whose draft this is. Without it Gmail opens the first signed-in account (u/0), which may not be the one holding the draft when several accounts share the browser.

## Output

- `sent` (boolean, required): True when the message was actually sent. Always true on success: the script fails loudly instead of returning false.
- `subject` (string | null, required): Subject of the message that was sent. Empty when the draft had no subject. For a reply, the subject it carries from its conversation.
- `threadId` (string, required): Conversation id, unchanged by sending, so the sent message can be located afterwards.
- `account_used` (string, required): The Gmail account the message was sent from, read from the session rather than assumed.
- `verified_on_page` (boolean, required): True when the send was confirmed by server-derived evidence: Gmail accepting it, or the message appearing in a settled Sent list (for a reply, together with the draft leaving Drafts).
- `recipientsDisplay` (string, required): The recipients as the compose window lists them: display names, which is what Gmail renders there. The addresses are in recipients.
- `sender` (string | null, optional): The address the message was sent from: the Gmail account whose mailbox held and sent the draft (same as account_used).
- `isReply` (boolean, optional): True when the draft was a reply saved inside a conversation, false for a new message.
- `attempts` (integer, optional): How many Send clicks it took before Gmail accepted. More than 1 means a click silently failed to reach the server and was retried.
- `leftDrafts` (boolean, optional): Whether the draft had disappeared from Drafts by the time this was checked. For a new message it is informational, since it depends on the list repainting. For a reply it is this very draft id, and it backs the Sent check.
- `recipients` (array, optional): The To addresses as the compose window holds them, so the delivery is auditable.
- `foundInSent` (boolean, optional): Whether the message was found in Sent afterwards, read only once the previous view's draft rows had cleared. For a new message, its conversation; for a reply, its conversation ending on a new message, since the conversation may have been in Sent before.
- `previousDraftId` (string, optional): The draft id that was sent and therefore no longer exists as a draft.
- `accepted_by_server` (boolean, optional): True when Gmail confirmed it accepted the send: the Undo link's target rewritten to a server-assigned conversation, or Gmail's answer listing the message under Sent.

## FAQ

### What does "Send a Gmail draft" do?

Send an existing Gmail draft, identified by the id the drafts listing gives you: a new message, or a reply saved inside a conversation. This delivers a real message and cannot be undone. The draft's recipients and subject are reported back with the send, and a draft with no recipient is refused rather than attempted. The call succeeds only once Gmail confirms the send; otherwise it fails and says whether anything may have gone out. The conversation id is returned and is the same before and after sending, so the message can be found again afterwards. Sending a reply opens its conversation, which marks it as read.

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
