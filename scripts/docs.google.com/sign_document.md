# Google Docs: sign a document sent for eSignature

Sign a Google Docs / Drive eSignature request addressed to the signed-in account: fills every field the signer has, on any page. Signature and initials are generated from the full name and initials you give, name fields print the full name, text fields take your values by field id (from get_signature_request), and date fields fill themselves. Then it completes the signing and checks the text Google received. Returns the account that signed, each field with its page (and text values), and how many other signers are still pending. Refuses when the account is not a signer, has already signed, or the request was cancelled, and when initials or a text value are needed but not given. Google asks the signer to accept its eSignature terms before completing: pass acceptTerms only when the user agrees to them, otherwise nothing is signed. When the browser is signed in to several Google accounts, pass the account to act as.

- Site: docs.google.com
- Address: `reduck/docs.google.com/sign_document`
- Updated: 2026-11-19 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/sign_document`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sign_document
```

## Input

- `url` (string, required): Link to the PDF to sign (https://drive.google.com/file/d/<id>/..., as list_signature_requests or request_signatures return) or the bare file id.
- `fullName` (string, required): Full name of the signer; Google draws the signature from it and prints it in name fields.
- `account` (string, optional): Google account to sign as when the browser is signed in to several.
- `initials` (string, optional): The signer's initials. Needed when the document has initials fields (get_signature_request lists them).
- `textFields` (array, optional): Values for the document's text fields, one per field, by the fieldId get_signature_request returns. Needed when the document has text fields.
- `acceptTerms` (boolean, optional): True when the user agrees to Google's eSignature terms of service, which Google asks to accept before completing a signature. Without it, the script stops at that step and signs nothing.

## Output

- `title` (string | null, required)
- `fileId` (string, required)
- `signed` (boolean, required)
- `signedAs` (string, required): Email of the account that signed.
- `otherSignersPending` (integer, required): Signers who have not signed yet, besides this account. When 0, Google emails the signed copy to everyone.
- `url` (string, optional)
- `fields` (array, optional): This signer's fields, from Google's data: type, page number, and for text fields the value Google received.
- `fieldsSigned` (integer, optional): Fields filled by this run (signatures, initials, names and text); date fields fill themselves and are not counted.

## FAQ

### What does "Google Docs: sign a document sent for eSignature" do?

Sign a Google Docs / Drive eSignature request addressed to the signed-in account: fills every field the signer has, on any page. Signature and initials are generated from the full name and initials you give, name fields print the full name, text fields take your values by field id (from get_signature_request), and date fields fill themselves. Then it completes the signing and checks the text Google received. Returns the account that signed, each field with its page (and text values), and how many other signers are still pending. Refuses when the account is not a signer, has already signed, or the request was cancelled, and when initials or a text value are needed but not given. Google asks the signer to accept its eSignature terms before completing: pass acceptTerms only when the user agrees to them, otherwise nothing is signed. When the browser is signed in to several Google accounts, pass the account to act as.

### What information do I need to provide?

Required: url, fullName. Optional: account, initials, textFields, acceptTerms.

### What does it return?

It returns url, title, fields, fileId, signed, signedAs, fieldsSigned, otherSignersPending.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It makes changes on docs.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sign_document, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sign_document

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/sign_document
