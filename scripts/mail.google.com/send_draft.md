# Send a Gmail draft

Automatically send a Gmail draft on mail.google.com. Send an existing Gmail draft, identified by the id the drafts listing gives you. This delivers a real message and cannot be undone, so the draft's recipients and subject are read and reported back before and with the send, and a draft with no recipient is refused rather than attempted. Success is confirmed two ways: the draft leaves Drafts and the same conversation turns up in Sent. The conversation id is returned and is the same before and after sending, so the message can be found again afterwards.

- Site: mail.google.com
- Address: `reduck/mail.google.com/send_draft`
- Updated: 2026-09-07 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/send_draft`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/send_draft
```

## Input

- `draftId` (string, required): The draft's current id, as returned by the drafts listing. Gmail replaces a draft's id every time it is saved, so use a freshly listed one.

## Output

- `sent` (boolean, required): True when the message was actually sent. Always true on success — the script fails loudly instead of returning false.
- `subject` (string | null, required): Subject of the message that was sent. Empty when the draft had no subject.
- `threadId` (string, required): Conversation id, unchanged by sending, so the sent message can be located afterwards.
- `account_used` (string, required): The Gmail account the message was sent from, read from the session rather than assumed.
- `verified_on_page` (boolean, required): True when the send was confirmed by server-derived evidence: the Undo link's target being rewritten to the server-assigned conversation, or the conversation appearing in a settled Sent list.
- `recipientsDisplay` (string, required): The recipients exactly as the compose window lists them — display names with the domain, which is what Gmail renders there. Full email addresses are not available on this surface, so none are invented; this is reported so the delivery is still auditable.
- `sender` (string | null, optional): The from address as the compose window shows it, read off the message itself rather than the browser session.
- `attempts` (integer, optional): How many Send clicks it took before Gmail accepted. More than 1 means a click silently failed to reach the server and was retried.
- `leftDrafts` (boolean, optional): Whether the draft had also disappeared from Drafts by the time this was checked. Informational only: it depends on the list repainting, so false here does not mean the send failed.
- `foundInSent` (boolean, optional): Whether the conversation was found in Sent afterwards, read only once the previous view's draft rows had cleared — an immediate read matches the draft's own row and proves nothing.
- `previousDraftId` (string, optional): The draft id that was sent and therefore no longer exists as a draft.
- `accepted_by_server` (boolean, optional): True when Gmail rewrote the Undo link's target from the local draft to a server-assigned conversation id, which is the direct signal that the send was accepted.

## FAQ

### What does "Send a Gmail draft" do?

Send an existing Gmail draft, identified by the id the drafts listing gives you. This delivers a real message and cannot be undone, so the draft's recipients and subject are read and reported back before and with the send, and a draft with no recipient is refused rather than attempted. Success is confirmed two ways: the draft leaves Drafts and the same conversation turns up in Sent. The conversation id is returned and is the same before and after sending, so the message can be found again afterwards.

### How do I automatically send a Gmail draft on mail.google.com?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/send_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/send_draft

### Is there a mail.google.com API to send a Gmail draft?

You do not need one. "Send a Gmail draft" drives the real mail.google.com pages in a browser, so it works whether or not mail.google.com offers an API for this.

### What information do I need to provide?

Required: draftId.

### What does it return?

It returns sent, sender, subject, attempts, threadId, leftDrafts, foundInSent, account_used, previousDraftId, verified_on_page, recipientsDisplay, accepted_by_server.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/send_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/send_draft

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/send_draft
