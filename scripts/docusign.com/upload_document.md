# DocuSign — upload a document as a draft envelope

Automatically upload a document as a draft envelope on docusign.com. Upload a document to DocuSign as a new draft envelope on the signed-in account and return the envelope id, the document's id and name, and its page count. It only creates the draft: no recipients are added and nothing is sent. Signed out is a clear error.

- Site: docusign.com
- Address: `reduck/docusign.com/upload_document`
- Updated: 2026-09-30 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docusign.com/upload_document`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docusign.com/upload_document
```

## Input

- `document` (string, required): The file to upload: PDF, Word, Excel, PowerPoint, image, text, etc.
- `documentName` (string, required): File name shown in DocuSign, with extension (e.g. "contract.pdf"). The extension tells DocuSign the file type.

## Output

- `status` (string, required)
- `document` (object, required)
- `accountId` (string, required)
- `envelopeId` (string, required)
- `draftUrl` (string, optional)

## FAQ

### What does "DocuSign — upload a document as a draft envelope" do?

Upload a document to DocuSign as a new draft envelope on the signed-in account and return the envelope id, the document's id and name, and its page count. It only creates the draft: no recipients are added and nothing is sent. Signed out is a clear error.

### How do I automatically upload a document as a draft envelope on docusign.com?

Ask an AI agent connected to Reduck to run reduck/docusign.com/upload_document, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docusign.com/upload_document

### Is there a docusign.com API to upload a document as a draft envelope?

You do not need one. "DocuSign — upload a document as a draft envelope" drives the real docusign.com pages in a browser, so it works whether or not docusign.com offers an API for this.

### What information do I need to provide?

Required: document, documentName.

### What does it return?

It returns status, document, draftUrl, accountId, envelopeId.

### Do I need to be logged in to docusign.com?

Yes. It acts as you on docusign.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docusign.com cookies saved by the Reduck extension.

### Does it change anything on docusign.com, or only read data?

It makes changes on docusign.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docusign.com/upload_document, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docusign.com/upload_document

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docusign.com/upload_document
