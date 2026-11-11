# Google Drive: get where a document must be signed

Automatically get where a document must be signed on docs.google.com. Read a Google Docs / Drive eSignature request without signing: who sent it, each signer and whether they have signed, and every field each signer must fill (signature, initials, date, name or text), with its page number and its position on the page (left, top, right, bottom as fractions of the page width and height, from the top-left corner). Text fields also come with their id (pass it to sign_document), the sender's hint, and the value once signed. Says which fields are for the signed-in account. Takes the PDF link from list_signature_requests or the request email. Refuses when the file has no signature request. When the browser is signed in to several Google accounts, pass the account to act as.

- Site: docs.google.com
- Address: `reduck/docs.google.com/get_signature_request`
- Updated: 2026-11-10 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/get_signature_request`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/get_signature_request
```

## Input

- `url` (string, required): Link to the PDF sent for signature (https://drive.google.com/file/d/<id>/..., as list_signature_requests returns) or the bare file id.
- `account` (string, optional): Google account to act as when the browser is signed in to several.

## Output

- `fileId` (string, required)
- `status` (string | null, required): The request's status as Google gives it (for example inProgress, approved).
- `signers` (array, required)
- `requestedBy` (string | null, required): Email of who sent the request.
- `title` (string | null, optional)

## FAQ

### What does "Google Drive: get where a document must be signed" do?

Read a Google Docs / Drive eSignature request without signing: who sent it, each signer and whether they have signed, and every field each signer must fill (signature, initials, date, name or text), with its page number and its position on the page (left, top, right, bottom as fractions of the page width and height, from the top-left corner). Text fields also come with their id (pass it to sign_document), the sender's hint, and the value once signed. Says which fields are for the signed-in account. Takes the PDF link from list_signature_requests or the request email. Refuses when the file has no signature request. When the browser is signed in to several Google accounts, pass the account to act as.

### How do I automatically get where a document must be signed on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/get_signature_request, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/get_signature_request

### Is there a docs.google.com API to get where a document must be signed?

You do not need one. "Google Drive: get where a document must be signed" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: account.

### What does it return?

It returns title, fileId, status, signers, requestedBy.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It only reads. It looks things up on docs.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/get_signature_request, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/get_signature_request

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/get_signature_request
