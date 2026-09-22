# Send Instagram DM

Automatically send Instagram DM on instagram.com. Send a DM to an Instagram user by their username: plain text, an image attachment, or both together. Takes the image as base64 so it runs from any client. Returns ids/timestamps for whichever parts were sent, and the recipient-side restriction banner if one is shown right after sending.

- Site: instagram.com
- Address: `reduck/instagram.com/send_message`
- Updated: 2026-09-18 (v22)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/send_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/send_message
```

## Input

- `username` (string, required): Instagram handle without @, e.g. f1
- `message` (string, optional): Plain text message to send. At least one of message or fileBase64 is required.
- `filename` (string, optional): Filename to send the attachment as, e.g. photo.png or clip.mp4. Required when fileBase64 is set.
- `mimeType` (string, optional): MIME type of the attachment; inferred from the filename extension when omitted.
- `threadUrl` (string, optional): Optional. An existing conversation URL (https://www.instagram.com/direct/t/<thread_id>/, from get_inbox). Use this to reach an account whose profile shows no Message control — a non-followed account renders only a Follow button, so the profile route cannot reach it even once a conversation exists.
- `fileBase64` (string, optional): Attachment contents, base64-encoded (no data: prefix). At least one of message or fileBase64 is required.

## Output

- `username` (string, required)
- `notice` (string | null, optional): Recipient-side restriction banner visible in the thread right after sending, else null. May lag the server push — null does not guarantee delivery.
- `message` (string | null, optional)
- `filename` (string | null, optional)
- `messageId` (string | null, optional): id of the sent text message, null if no message was sent
- `timestampMs` (number | null, optional)
- `mediaMessageId` (string | null, optional): id of the sent image message, null if no image was sent
- `mediaTimestampMs` (number | null, optional)

## FAQ

### What does "Send Instagram DM" do?

Send a DM to an Instagram user by their username: plain text, an image attachment, or both together. Takes the image as base64 so it runs from any client. Returns ids/timestamps for whichever parts were sent, and the recipient-side restriction banner if one is shown right after sending.

### How do I automatically send Instagram DM on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/send_message

### Is there a instagram.com API to send Instagram DM?

You do not need one. "Send Instagram DM" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: message, filename, mimeType, threadUrl, fileBase64.

### What does it return?

It returns notice, message, filename, username, messageId, timestampMs, mediaMessageId, mediaTimestampMs.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/send_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/send_message
