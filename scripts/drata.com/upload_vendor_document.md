# Upload a document to a Drata vendor

Automatically upload a document to a Drata vendor on drata.com. Uploads a file (a DPA, a SOC 2 report, a certificate) to a vendor's Reports and documents tab in Drata, through the Add files dialog. Takes the vendor number from its Drata page URL and keeps the file's own name. Returns the document as Drata stores it. Requires being signed in to Drata.

- Site: drata.com
- Address: `reduck/drata.com/upload_vendor_document`
- Updated: 2026-11-17 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drata.com/upload_vendor_document`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drata.com/upload_vendor_document
```

## Input

- `file` (string, required): The document file.
- `vendorId` (integer, required): The vendor number in its Drata page URL: .../vendors/current/<number>/overview.
- `workspacePath` (string, required): The part of the Drata app URL after app2.drata.com/main/, up to and including the workspace number, e.g. NA/acme/1.

## Output

- `status` (integer, required)
- `uploaded` (boolean, required)
- `document` (object | null, optional)

## FAQ

### What does "Upload a document to a Drata vendor" do?

Uploads a file (a DPA, a SOC 2 report, a certificate) to a vendor's Reports and documents tab in Drata, through the Add files dialog. Takes the vendor number from its Drata page URL and keeps the file's own name. Returns the document as Drata stores it. Requires being signed in to Drata.

### How do I automatically upload a document to a Drata vendor on drata.com?

Ask an AI agent connected to Reduck to run reduck/drata.com/upload_vendor_document, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/upload_vendor_document

### Is there a drata.com API to upload a document to a Drata vendor?

You do not need one. "Upload a document to a Drata vendor" drives the real drata.com pages in a browser, so it works whether or not drata.com offers an API for this.

### What information do I need to provide?

Required: workspacePath, vendorId, file.

### What does it return?

It returns status, document, uploaded.

### Do I need to be logged in to drata.com?

Yes. It acts as you on drata.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drata.com cookies saved by the Reduck extension.

### Does it change anything on drata.com, or only read data?

It makes changes on drata.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drata.com/upload_vendor_document, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/upload_vendor_document

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drata.com/upload_vendor_document
