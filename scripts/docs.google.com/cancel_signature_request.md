# Google Drive: cancel a signature request you sent

Automatically cancel a signature request you sent on docs.google.com. Cancel a Google Docs / Drive eSignature request that the signed-in account sent, with an optional message to the signers. Signers who have not signed can no longer sign it. Takes the PDF link returned by request_signatures or list_signature_requests (which = sent). Returns the request's status afterwards. Refuses when the account did not send the request, or the request is already completed or cancelled. When the browser is signed in to several Google accounts, pass the account to act as.

- Site: docs.google.com
- Address: `reduck/docs.google.com/cancel_signature_request`
- Updated: 2026-11-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/cancel_signature_request`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/cancel_signature_request
```

## Input

- `url` (string, required): Link to the PDF sent for signature (https://drive.google.com/file/d/<id>/...) or the bare file id.
- `account` (string, optional): Google account to act as when the browser is signed in to several.
- `message` (string, optional): Optional message shown to the signers with the cancellation.

## Output

- `fileId` (string, required)
- `cancelled` (boolean, required)
- `cancelledBy` (string, required)
- `url` (string, optional)
- `title` (string | null, optional)
- `message` (string | null, optional): The message Google received with the cancellation.
- `signersPending` (integer, optional): Signers who had not signed when it was cancelled.

## FAQ

### What does "Google Drive: cancel a signature request you sent" do?

Cancel a Google Docs / Drive eSignature request that the signed-in account sent, with an optional message to the signers. Signers who have not signed can no longer sign it. Takes the PDF link returned by request_signatures or list_signature_requests (which = sent). Returns the request's status afterwards. Refuses when the account did not send the request, or the request is already completed or cancelled. When the browser is signed in to several Google accounts, pass the account to act as.

### How do I automatically cancel a signature request you sent on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/cancel_signature_request, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/cancel_signature_request

### Is there a docs.google.com API to cancel a signature request you sent?

You do not need one. "Google Drive: cancel a signature request you sent" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: account, message.

### What does it return?

It returns url, title, fileId, message, cancelled, cancelledBy, signersPending.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It makes changes on docs.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/cancel_signature_request, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/cancel_signature_request

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/cancel_signature_request
