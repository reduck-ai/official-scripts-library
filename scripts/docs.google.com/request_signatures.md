# Google Docs: request eSignatures on a document

Automatically request eSignatures on a document on docs.google.com. Send a Google Doc out for eSignature: Google makes a PDF copy and emails each signer a link to sign it. Signers are given in the order of the document's signer roles. When the document has no fields yet, it adds one signer role per email (up to 10, all different), named after the signer, and one Signature field per signer. Pass signatureLine (for example the underscores after "Signature:") to put each signer's box on the document's own signature lines, in order; without it the boxes go at the end of the document with the signer's name above each. Pass signerNames to use names instead of emails. Returns the PDF's link, which sign_document, get_signature_request and cancel_signature_request take. Google asks to confirm before sharing with signers outside the sender's organisation: pass allowExternal only when the user agrees, otherwise nothing is sent. Use dryRun to check the request without sending it. Needs edit access and a Google account that has eSignature (most Workspace plans and Google One Premium). When the browser is signed in to several Google accounts, pass the account to act as.

- Site: docs.google.com
- Address: `reduck/docs.google.com/request_signatures`
- Updated: 2026-11-17 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/request_signatures`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/request_signatures
```

## Input

- `url` (string, required): Link to the Google Doc (https://docs.google.com/document/d/<id>/...) or the bare document id.
- `signers` (array, required): Signer emails, all different, one per signer role, in order. When the document has fields already, the count must match its signer roles; when it has none, one role (named after the signer) and one Signature field per email are added.
- `dryRun` (boolean, optional): True fills in the request and reads it back, then cancels: nothing is added to the document and nothing is sent. Pass false to send.
- `account` (string, optional): Google account to act as when the browser is signed in to several.
- `message` (string, optional): Message in the email to signers. It does not appear in the signed document.
- `reminders` (boolean, optional): Send automatic reminders to signers who have not signed.
- `signerNames` (array, optional): Signer names, same order and count as signers, used for the role names and, without signatureLine, the line above each added Signature box. Without it the email is used. Only used when the script adds the fields.
- `documentName` (string, optional): Name of the PDF to sign. Google's default is the document title with the date and time.
- `allowExternal` (boolean, optional): True when the user agrees to share the PDF with signers outside the sender's organisation, which Google asks to confirm. Without it, such a request stops and nothing is sent.
- `signatureLine` (string, optional): Text that marks each signer's signature line in the document, for example the underscores after "Signature:". Each signer's box replaces one occurrence, in order: the first signer gets the first occurrence, and so on. The document needs at least one occurrence per signer. Without it, the boxes go at the end of the document under each signer's name. Only used when the script adds the fields.

## Output

- `id` (string, required)
- `sent` (boolean, required): True when the request was sent.
- `pdfUrl` (string | null, required): Link to the PDF sent for signature; null in a dry run.
- `signers` (array, required)
- `fieldAdded` (boolean, required): True when a Signature field was added at the end of the document (or, in a dry run, would be).
- `accountUsed` (string | null, required)
- `signerRoles` (array, required): The signer roles the document has fields for, as Google names them.
- `pdfId` (string | null, optional)

## FAQ

### What does "Google Docs: request eSignatures on a document" do?

Send a Google Doc out for eSignature: Google makes a PDF copy and emails each signer a link to sign it. Signers are given in the order of the document's signer roles. When the document has no fields yet, it adds one signer role per email (up to 10, all different), named after the signer, and one Signature field per signer. Pass signatureLine (for example the underscores after "Signature:") to put each signer's box on the document's own signature lines, in order; without it the boxes go at the end of the document with the signer's name above each. Pass signerNames to use names instead of emails. Returns the PDF's link, which sign_document, get_signature_request and cancel_signature_request take. Google asks to confirm before sharing with signers outside the sender's organisation: pass allowExternal only when the user agrees, otherwise nothing is sent. Use dryRun to check the request without sending it. Needs edit access and a Google account that has eSignature (most Workspace plans and Google One Premium). When the browser is signed in to several Google accounts, pass the account to act as.

### How do I automatically request eSignatures on a document on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/request_signatures, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/request_signatures

### Is there a docs.google.com API to request eSignatures on a document?

You do not need one. "Google Docs: request eSignatures on a document" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Required: url, signers. Optional: dryRun, account, message, reminders, signerNames, documentName, allowExternal, signatureLine.

### What does it return?

It returns id, sent, pdfId, pdfUrl, signers, fieldAdded, accountUsed, signerRoles.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It makes changes on docs.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/request_signatures, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/request_signatures

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/request_signatures
