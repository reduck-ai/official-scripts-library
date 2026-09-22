# Download an Atlassian invoice PDF

Automatically download an Atlassian invoice PDF on admin.atlassian.com. Download one Atlassian (admin.atlassian.com) billing invoice, given the downloadUrl — or the id plus transaction_account — that admin.atlassian.com/list_invoices returns. Returns the real filename plus the PDF bytes as base64 (decode and write it yourself). The bytes come back with the run, so it does not depend on the browser's own download folder, and it still works when Atlassian serves the PDF from a signed storage location. Only an org billing admin can download invoices.

- Site: admin.atlassian.com
- Address: `reduck/admin.atlassian.com/download_invoice`
- Updated: 2026-08-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/admin.atlassian.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/admin.atlassian.com/download_invoice
```

## Input

- `id` (string, optional): Atlassian invoice id from admin.atlassian.com/list_invoices. Used only when downloadUrl is not given, and then transaction_account is required too.
- `number` (string, optional): The invoice's number from the list row (e.g. IN-EU-002-392-813). Optional, and only used to name the file: Atlassian's download endpoint sends no Content-Disposition, so without this the filename falls back to the opaque invoice id.
- `downloadUrl` (string, optional): The invoice's downloadUrl exactly as returned by admin.atlassian.com/list_invoices. Preferred over id/transaction_account.
- `sourceSystem` (string, optional): Which billing system issued the invoice, from the list row. Only used when building the URL from id.
- `transaction_account` (string, optional): The invoice's transaction_account from the list row. Required when using id instead of downloadUrl.

## Output

- `filename` (string, required): The real suggested filename from the file's Content-Disposition, falling back to Atlassian-<id>.pdf.
- `pdf_base64` (string, required): The PDF bytes, base64-encoded. Decode and write it yourself — the script is sandboxed and cannot write to disk.
- `via` (string, optional): Which route produced the bytes: a direct same-origin fetch of the billing endpoint, or a second fetch after landing on the storage host Atlassian redirected the file to. Diagnostic only.
- `size_bytes` (integer, optional): Byte length of the decoded PDF.

## FAQ

### What does "Download an Atlassian invoice PDF" do?

Download one Atlassian (admin.atlassian.com) billing invoice, given the downloadUrl — or the id plus transaction_account — that admin.atlassian.com/list_invoices returns. Returns the real filename plus the PDF bytes as base64 (decode and write it yourself). The bytes come back with the run, so it does not depend on the browser's own download folder, and it still works when Atlassian serves the PDF from a signed storage location. Only an org billing admin can download invoices.

### How do I automatically download an Atlassian invoice PDF on admin.atlassian.com?

Ask an AI agent connected to Reduck to run reduck/admin.atlassian.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.atlassian.com/download_invoice

### Is there a admin.atlassian.com API to download an Atlassian invoice PDF?

You do not need one. "Download an Atlassian invoice PDF" drives the real admin.atlassian.com pages in a browser, so it works whether or not admin.atlassian.com offers an API for this.

### What information do I need to provide?

Optional: id, number, downloadUrl, sourceSystem, transaction_account.

### What does it return?

It returns via, filename, pdf_base64, size_bytes.

### Do I need to be logged in to admin.atlassian.com?

Yes. It acts as you on admin.atlassian.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the admin.atlassian.com cookies saved by the Reduck extension.

### Does it change anything on admin.atlassian.com, or only read data?

It only reads. It looks things up on admin.atlassian.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/admin.atlassian.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/admin.atlassian.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/admin.atlassian.com/download_invoice
