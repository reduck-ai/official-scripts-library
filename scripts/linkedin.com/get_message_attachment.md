# Download a LinkedIn message attachment

Automatically download a LinkedIn message attachment on linkedin.com. Download the file attached to a message in a classic LinkedIn messaging thread. Returns filename, mimeType, size and the bytes as base64, plus the direct URL. Omit the message urn to take the most recent message in the thread that carries an attachment.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_message_attachment`
- Updated: 2026-09-03 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_message_attachment`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_message_attachment
```

## Input

- `threadUrl` (string, required): Conversation thread URL from list_inbox.
- `maxBytes` (integer, optional): Refuse to base64-encode anything larger than this. Default 8000000 (8 MB); the URL is still returned.
- `messageUrn` (string, optional): Message identifier to pull from (as returned by this script's own output, or by react_to_message). Omit to take the newest message carrying an attachment.

## Output

- `url` (string, required)
- `threadUrl` (string, required)
- `messageUrn` (string, required)
- `kind` (string, optional): image = rendered inline; file = a document card with a download link.
- `size` (integer | null, optional)
- `base64` (string | null, optional): Bytes, base64-encoded. Null when the file exceeded maxBytes — url is still usable.
- `filename` (string | null, optional)
- `mimeType` (string | null, optional)
- `pickedLatest` (boolean, optional)
- `skippedEncoding` (boolean, optional)

## FAQ

### What does "Download a LinkedIn message attachment" do?

Download the file attached to a message in a classic LinkedIn messaging thread. Returns filename, mimeType, size and the bytes as base64, plus the direct URL. Omit the message urn to take the most recent message in the thread that carries an attachment.

### How do I automatically download a LinkedIn message attachment on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_message_attachment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_message_attachment

### Is there a linkedin.com API to download a LinkedIn message attachment?

You do not need one. "Download a LinkedIn message attachment" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: threadUrl. Optional: maxBytes, messageUrn.

### What does it return?

It returns url, kind, size, base64, filename, mimeType, threadUrl, messageUrn, pickedLatest, skippedEncoding.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_message_attachment, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_message_attachment

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_message_attachment
