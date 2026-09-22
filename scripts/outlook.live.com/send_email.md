# Send an Outlook.com email

Automatically send an Outlook.com email on outlook.live.com. Send an email from Outlook.com (outlook.live.com) to a recipient, with a subject and body. Confirms the message actually left by finding it in Sent Items, rather than assuming the Send click worked.

- Site: outlook.live.com
- Address: `reduck/outlook.live.com/send_email`
- Updated: 2026-09-16 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/outlook.live.com/send_email`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/send_email
```

## Input

- `to` (string, required): Recipient email address, e.g. someone@example.com
- `body` (string, optional): Plain text body of the message. Give a subject, a body, or both — a message with neither cannot be identified in Sent Items afterwards, so the send could not be confirmed.
- `subject` (string, optional): Subject line. Give a subject, a body, or both — a message with neither cannot be identified in Sent Items afterwards, so the send could not be confirmed.
- `sentFolder` (string, optional): Name of the sent-mail folder as shown in your folder list, used to confirm the message left. Override this if your mailbox is not in English.

## Output

- `to` (string, required)
- `sent` (boolean, required): True only when the message was found in Sent Items afterwards. Never inferred from the Send click.
- `subject` (string | null, required)
- `body` (string | null, optional)
- `sentId` (string | null, optional): Row id of the message in Sent Items.
- `composed` (object | null, optional): What the composer held just before sending. Separates a fill failure from a send failure.
- `unsentReason` (string | null, optional)
- `confirmationDialog` (boolean, optional): Whether Outlook asked for confirmation before sending, which it does when the message has no subject. It is confirmed automatically; the message is sent either way.

## FAQ

### What does "Send an Outlook.com email" do?

Send an email from Outlook.com (outlook.live.com) to a recipient, with a subject and body. Confirms the message actually left by finding it in Sent Items, rather than assuming the Send click worked.

### How do I automatically send an Outlook.com email on outlook.live.com?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/send_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/send_email

### Is there a outlook.live.com API to send an Outlook.com email?

You do not need one. "Send an Outlook.com email" drives the real outlook.live.com pages in a browser, so it works whether or not outlook.live.com offers an API for this.

### What information do I need to provide?

Required: to. Optional: body, subject, sentFolder.

### What does it return?

It returns to, body, sent, sentId, subject, composed, unsentReason, confirmationDialog.

### Do I need to be logged in to outlook.live.com?

Yes. It acts as you on outlook.live.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the outlook.live.com cookies saved by the Reduck extension.

### Does it change anything on outlook.live.com, or only read data?

It makes changes on outlook.live.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/send_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/send_email

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/outlook.live.com/send_email
