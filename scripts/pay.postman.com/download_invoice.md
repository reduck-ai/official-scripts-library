# Postman: download invoice PDF

Automatically download invoice PDF on pay.postman.com. Downloads a Postman invoice PDF given its public viewUrl (from postman.co/list_invoices). The download itself is reliable; occasionally the confirmation step doesn't complete, in which case status is reported as unconfirmed even though the file was saved successfully.

- Site: pay.postman.com
- Address: `reduck/pay.postman.com/download_invoice`
- Updated: 2026-08-26 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pay.postman.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pay.postman.com/download_invoice
```

## Input

- `viewUrl` (string, required): Public tokenized invoice page, e.g. https://pay.postman.com/invoices/view?invoice_public_id=inv_XXXX (from postman.co/list_invoices' viewUrl field).

## Output

- `status` (string, required): confirmed: Reduck retrieved download metadata. unconfirmed: the fetch+download succeeded but Reduck's confirmation step failed to resolve — the file has still reliably landed in the browser's download location.
- `filename` (string, required): Saved file name, e.g. inv_XXXX.pdf.
- `url` (string | null, optional): Download link (cloud-browser sessions). Null when unconfirmed.
- `note` (string | null, optional): Present when status is unconfirmed — the last error hit while trying to confirm.
- `path` (string | null, optional): Local file path (agent machine, or the user's machine for a device session). Null when unconfirmed.

## FAQ

### What does "Postman: download invoice PDF" do?

Downloads a Postman invoice PDF given its public viewUrl (from postman.co/list_invoices). The download itself is reliable; occasionally the confirmation step doesn't complete, in which case status is reported as unconfirmed even though the file was saved successfully.

### How do I automatically download invoice PDF on pay.postman.com?

Ask an AI agent connected to Reduck to run reduck/pay.postman.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pay.postman.com/download_invoice

### Is there a pay.postman.com API to download invoice PDF?

You do not need one. "Postman: download invoice PDF" drives the real pay.postman.com pages in a browser, so it works whether or not pay.postman.com offers an API for this.

### What information do I need to provide?

Required: viewUrl.

### What does it return?

It returns url, note, path, status, filename.

### Do I need to be logged in to pay.postman.com?

No. It only uses pages of pay.postman.com that are reachable without signing in.

### Does it change anything on pay.postman.com, or only read data?

It only reads. It looks things up on pay.postman.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pay.postman.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pay.postman.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pay.postman.com/download_invoice
