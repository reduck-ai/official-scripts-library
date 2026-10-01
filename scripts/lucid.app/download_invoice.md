# Download a Lucid invoice PDF

Automatically download a Lucid invoice PDF on lucid.app. Download one Lucid (Lucidchart/Lucidspark) billing invoice PDF, given the invoice number that lucid.app/list_invoices returns. Returns the filename plus the PDF bytes as base64 (decode and write it yourself). A number that does not match an invoice fails with a clear error. Works whatever language the account is set to. Pass pdfUrl (returned by a previous run) instead of number to download it directly.

- Site: lucid.app
- Address: `reduck/lucid.app/download_invoice`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lucid.app/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lucid.app/download_invoice
```

## Input

- `number` (string, optional): The invoice number as returned by lucid.app/list_invoices (e.g. 19888678). The invoices table is opened and the row with this number is downloaded. Required unless pdfUrl is given.
- `pdfUrl` (string, optional): A direct Lucid invoice PDF URL (https://payment.lucid.app/accounts/<accountId>/pdfInvoice/<number>), if you already have one. Skips opening the billing UI entirely.

## Output

- `filename` (string, required): Filename from the file's Content-Disposition, falling back to Lucidchart-<number>.pdf. Lucid's own suggested name is the bare invoice number with no extension, so it is not used as-is.
- `pdf_base64` (string, required): The PDF bytes, base64-encoded. Decode and write it yourself — the script is sandboxed and cannot write to disk.
- `number` (string | null, optional): The invoice number that was downloaded.
- `pdfUrl` (string, optional): The PDF URL the bytes were read from — reusable as this script's pdfUrl input to skip the UI next time.
- `size_bytes` (integer, optional): Byte length of the decoded PDF.

## FAQ

### What does "Download a Lucid invoice PDF" do?

Download one Lucid (Lucidchart/Lucidspark) billing invoice PDF, given the invoice number that lucid.app/list_invoices returns. Returns the filename plus the PDF bytes as base64 (decode and write it yourself). A number that does not match an invoice fails with a clear error. Works whatever language the account is set to. Pass pdfUrl (returned by a previous run) instead of number to download it directly.

### How do I automatically download a Lucid invoice PDF on lucid.app?

Ask an AI agent connected to Reduck to run reduck/lucid.app/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lucid.app/download_invoice

### Is there a lucid.app API to download a Lucid invoice PDF?

You do not need one. "Download a Lucid invoice PDF" drives the real lucid.app pages in a browser, so it works whether or not lucid.app offers an API for this.

### What information do I need to provide?

Optional: number, pdfUrl.

### What does it return?

It returns number, pdfUrl, filename, pdf_base64, size_bytes.

### Do I need to be logged in to lucid.app?

Yes. It acts as you on lucid.app: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the lucid.app cookies saved by the Reduck extension.

### Does it change anything on lucid.app, or only read data?

It only reads. It looks things up on lucid.app and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lucid.app/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lucid.app/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/lucid.app/download_invoice
