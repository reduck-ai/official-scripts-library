# unsubscribe_from_sender

Unsubscribe from a mailing list using Gmail's own unsubscribe control, which appears beside the sender on a message carrying a List-Unsubscribe header. Returns the sender it acted on, whether the control was present, and whether Gmail confirmed the request. This leaves the mailing list for real and cannot be undone from Gmail: confirm the exact sender with the user before running, and note that approval for one sender does not carry over to another. Senders with no unsubscribe control are reported rather than acted on, and the script never falls back to reporting spam.

- Site: mail.google.com
- Address: `reduck/mail.google.com/unsubscribe_from_sender`
- Updated: 2026-09-07 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mail.google.com/unsubscribe_from_sender`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mail.google.com/unsubscribe_from_sender
```

## Input

- `threadId` (string, required): A thread from the sender to unsubscribe from, as returned by mail.google.com/search_emails (its threadId field).
- `expectedSender` (string, required): The sender address the thread is expected to be from, asserted against the message before anything is clicked, so a stale thread id cannot unsubscribe you from the wrong list.
- `account` (string, optional): Optional authuser value for a browser signed into several Google accounts. Omit for the default (u/0).

## Output

- `sender` (string, required): The sender address read from the message, not echoed from the input.
- `threadId` (string, required)
- `unsubscribed` (boolean, required): Whether the unsubscribe was confirmed to Gmail. False when the sender offers no control, or only an off-Gmail one (see requires_sender_website).
- `control_present` (boolean, required): Whether Gmail offered an unsubscribe control for this sender at all.
- `link_gone` (boolean | null, optional): Whether the unsubscribe control disappeared afterwards, which is Gmail's own signal that the request was accepted.
- `confirmation` (string | null, optional): Gmail's own wording, quoted for the record rather than matched against.
- `requires_sender_website` (boolean, optional): True when Gmail has no one-click unsubscribe for this sender and only offers to send you to the sender's own website. Nothing was clicked through: finishing an unsubscribe on a third-party site is the caller's decision.

## FAQ

### What does "unsubscribe_from_sender" do?

Unsubscribe from a mailing list using Gmail's own unsubscribe control, which appears beside the sender on a message carrying a List-Unsubscribe header. Returns the sender it acted on, whether the control was present, and whether Gmail confirmed the request. This leaves the mailing list for real and cannot be undone from Gmail: confirm the exact sender with the user before running, and note that approval for one sender does not carry over to another. Senders with no unsubscribe control are reported rather than acted on, and the script never falls back to reporting spam.

### What information do I need to provide?

Required: threadId, expectedSender. Optional: account.

### What does it return?

It returns sender, threadId, link_gone, confirmation, unsubscribed, control_present, requires_sender_website.

### Do I need to be logged in to mail.google.com?

Yes. It acts as you on mail.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the mail.google.com cookies saved by the Reduck extension.

### Does it change anything on mail.google.com, or only read data?

It makes changes on mail.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mail.google.com/unsubscribe_from_sender, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mail.google.com/unsubscribe_from_sender

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/mail.google.com/unsubscribe_from_sender
