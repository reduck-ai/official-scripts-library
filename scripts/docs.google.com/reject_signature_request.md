# Google Drive: reject a signature request

Reject (decline to sign) a Google Docs / Drive eSignature request addressed to the signed-in account. Google then cancels the whole request for every signer. Takes the PDF link from list_signature_requests or the request email. Returns the account that rejected and the request's status afterwards. Refuses when the account is not a signer, has already signed or rejected, or the request is no longer open. When the browser is signed in to several Google accounts, pass the account to act as.

- Site: docs.google.com
- Address: `reduck/docs.google.com/reject_signature_request`
- Updated: 2026-11-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/reject_signature_request`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/reject_signature_request
```

## Input

- `url` (string, required): Link to the PDF sent for signature (https://drive.google.com/file/d/<id>/...) or the bare file id.
- `account` (string, optional): Google account to act as when the browser is signed in to several.

## Output

- `fileId` (string, required)
- `rejected` (boolean, required)
- `rejectedBy` (string, required)
- `url` (string, optional)
- `title` (string | null, optional)
- `requestedBy` (string | null, optional)

## FAQ

### What does "Google Drive: reject a signature request" do?

Reject (decline to sign) a Google Docs / Drive eSignature request addressed to the signed-in account. Google then cancels the whole request for every signer. Takes the PDF link from list_signature_requests or the request email. Returns the account that rejected and the request's status afterwards. Refuses when the account is not a signer, has already signed or rejected, or the request is no longer open. When the browser is signed in to several Google accounts, pass the account to act as.

### What information do I need to provide?

Required: url. Optional: account.

### What does it return?

It returns url, title, fileId, rejected, rejectedBy, requestedBy.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It makes changes on docs.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/reject_signature_request, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/reject_signature_request

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/reject_signature_request
