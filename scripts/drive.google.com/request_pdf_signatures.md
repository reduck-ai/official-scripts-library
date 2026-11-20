# Google Drive: request eSignatures on a PDF

Automatically request eSignatures on a PDF on drive.google.com. Send a PDF stored in Google Drive out for eSignature: places each field you give (signature, initials, name, text or date) on its page and position for its signer, then Google makes a copy of the PDF and emails each signer a link to sign it. Positions are fractions of the page width and height from the top-left corner, as get_signature_request returns them. Signers are numbered in the order given (signer 1 is the first email); up to 10. Returns the copy's link, which sign_document signs (send it to yourself to sign your own PDF). Google asks to confirm before sharing with signers outside the sender's organisation: pass allowExternal only when the user agrees, otherwise nothing is sent. Use dryRun to place the fields and fill the request without sending it. Needs a Google account that has eSignature. When the browser is signed in to several Google accounts, pass the account to act as.

- Site: drive.google.com
- Address: `reduck/drive.google.com/request_pdf_signatures`
- Updated: 2026-11-19 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drive.google.com/request_pdf_signatures`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drive.google.com/request_pdf_signatures
```

## Input

- `url` (string, required): Link to the PDF in Google Drive (https://drive.google.com/file/d/<id>/...) or the bare file id.
- `fields` (array, required): Fields to place. Every signer needs at least one signature field.
- `signers` (array, required): Signer emails; the first is signer 1, and so on.
- `dryRun` (boolean, optional): True places the fields and fills the request, then cancels: nothing is sent and the PDF is unchanged. Pass false to send.
- `account` (string, optional): Google account to act as when the browser is signed in to several.
- `message` (string, optional): Message in the email to signers.
- `reminders` (boolean, optional): Send automatic reminders to signers who have not signed.
- `documentName` (string, optional): Name of the copy to sign. Google's default is the PDF's name with the date and time.
- `allowExternal` (boolean, optional): True when the user agrees to share the PDF with signers outside the sender's organisation, which Google asks to confirm. Without it, such a request stops and nothing is sent.

## Output

- `sent` (boolean, required)
- `fields` (array, required): The fields as Google received them (in a dry run, as placed).
- `fileId` (string, required): The PDF the request was made from.
- `signers` (array, required)
- `pdfId` (string | null, optional): The copy to sign; pass it to sign_document. Null in a dry run.
- `pdfUrl` (string | null, optional)
- `accountUsed` (string | null, optional)

## FAQ

### What does "Google Drive: request eSignatures on a PDF" do?

Send a PDF stored in Google Drive out for eSignature: places each field you give (signature, initials, name, text or date) on its page and position for its signer, then Google makes a copy of the PDF and emails each signer a link to sign it. Positions are fractions of the page width and height from the top-left corner, as get_signature_request returns them. Signers are numbered in the order given (signer 1 is the first email); up to 10. Returns the copy's link, which sign_document signs (send it to yourself to sign your own PDF). Google asks to confirm before sharing with signers outside the sender's organisation: pass allowExternal only when the user agrees, otherwise nothing is sent. Use dryRun to place the fields and fill the request without sending it. Needs a Google account that has eSignature. When the browser is signed in to several Google accounts, pass the account to act as.

### How do I automatically request eSignatures on a PDF on drive.google.com?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/request_pdf_signatures, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/request_pdf_signatures

### Is there a drive.google.com API to request eSignatures on a PDF?

You do not need one. "Google Drive: request eSignatures on a PDF" drives the real drive.google.com pages in a browser, so it works whether or not drive.google.com offers an API for this.

### What information do I need to provide?

Required: url, signers, fields. Optional: dryRun, account, message, reminders, documentName, allowExternal.

### What does it return?

It returns sent, pdfId, fields, fileId, pdfUrl, signers, accountUsed.

### Do I need to be logged in to drive.google.com?

Yes. It acts as you on drive.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drive.google.com cookies saved by the Reduck extension.

### Does it change anything on drive.google.com, or only read data?

It makes changes on drive.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/request_pdf_signatures, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/request_pdf_signatures

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drive.google.com/request_pdf_signatures
