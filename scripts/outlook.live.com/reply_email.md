# Reply to an Outlook.com email

Automatically reply to an Outlook.com email on outlook.live.com. Reply to one Outlook.com (outlook.live.com) message by its id (from list_emails), optionally replying to all recipients. Confirms the reply actually left by finding it in Sent Items. Opening the message to reply marks it read, as it would in the UI.

- Site: outlook.live.com
- Address: `reduck/outlook.live.com/reply_email`
- Updated: 2026-09-16 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/outlook.live.com/reply_email`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/reply_email
```

## Input

- `id` (string, required): Message id from list_emails (the row's id attribute).
- `body` (string, required): Plain text body of the reply. Required: it is also what identifies the sent reply afterwards.
- `folder` (string, optional): Folder the message is in, as shown in your folder list.
- `replyAll` (boolean, optional): Reply to every recipient rather than just the sender.
- `sentFolder` (string, optional): Sent-mail folder name as shown in your folder list, used to confirm the reply left.

## Output

- `id` (string, required)
- `sent` (boolean, required): True only when the reply was found in the sent folder, with the folder switch itself verified first. Never inferred from the send keystroke.
- `body` (string, optional)
- `composed` (object | null, optional)
- `replyAll` (boolean, optional)
- `sentRowId` (string | null, optional): Row id of the reply in the sent folder. Outlook groups by CONVERSATION, so this is normally the same id as the message replied to — that is expected, not an error.
- `unsentReason` (string | null, optional)

## FAQ

### What does "Reply to an Outlook.com email" do?

Reply to one Outlook.com (outlook.live.com) message by its id (from list_emails), optionally replying to all recipients. Confirms the reply actually left by finding it in Sent Items. Opening the message to reply marks it read, as it would in the UI.

### How do I automatically reply to an Outlook.com email on outlook.live.com?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/reply_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/reply_email

### Is there a outlook.live.com API to reply to an Outlook.com email?

You do not need one. "Reply to an Outlook.com email" drives the real outlook.live.com pages in a browser, so it works whether or not outlook.live.com offers an API for this.

### What information do I need to provide?

Required: id, body. Optional: folder, replyAll, sentFolder.

### What does it return?

It returns id, body, sent, composed, replyAll, sentRowId, unsentReason.

### Do I need to be logged in to outlook.live.com?

Yes. It acts as you on outlook.live.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the outlook.live.com cookies saved by the Reduck extension.

### Does it change anything on outlook.live.com, or only read data?

It makes changes on outlook.live.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/outlook.live.com/reply_email, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/outlook.live.com/reply_email

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/outlook.live.com/reply_email
