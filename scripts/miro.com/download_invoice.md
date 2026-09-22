# Download a Miro invoice PDF

Automatically download a Miro invoice PDF on miro.com. Download one Miro company billing invoice PDF, given the pdfUrl that miro.com/list_invoices returns. Saves the file to the device and returns its real filename plus the path it was saved to. Unlike the other download_invoice scripts it hands back a file on disk rather than the bytes inline, because Miro only releases these PDFs through a real browser download — so read the file from the returned path. Requires access to Miro company billing.

- Site: miro.com
- Address: `reduck/miro.com/download_invoice`
- Updated: 2026-09-08 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/miro.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/miro.com/download_invoice
```

## Input

- `pdfUrl` (string, required): The invoice's pdfUrl exactly as returned by miro.com/list_invoices (Miro's own billing payload supplies it). There is no way to derive this from an invoice id alone, so it is required.
- `id` (string, optional): The invoice id from the list row. Optional, used only to name the file when Miro's own download carries no real name.

## Output

- `path` (string, required): Path on the device the PDF was saved to. Miro's PDFs go through the device download bridge rather than coming back as base64 — see the description.
- `filename` (string, required): The invoice's real filename, taken from the basename of the saved file. Neither the bridge's own filename field nor Miro's suggested name is usable: both are content-addressed hashes.

## FAQ

### What does "Download a Miro invoice PDF" do?

Download one Miro company billing invoice PDF, given the pdfUrl that miro.com/list_invoices returns. Saves the file to the device and returns its real filename plus the path it was saved to. Unlike the other download_invoice scripts it hands back a file on disk rather than the bytes inline, because Miro only releases these PDFs through a real browser download — so read the file from the returned path. Requires access to Miro company billing.

### How do I automatically download a Miro invoice PDF on miro.com?

Ask an AI agent connected to Reduck to run reduck/miro.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/miro.com/download_invoice

### Is there a miro.com API to download a Miro invoice PDF?

You do not need one. "Download a Miro invoice PDF" drives the real miro.com pages in a browser, so it works whether or not miro.com offers an API for this.

### What information do I need to provide?

Required: pdfUrl. Optional: id.

### What does it return?

It returns path, filename.

### Do I need to be logged in to miro.com?

Yes. It acts as you on miro.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the miro.com cookies saved by the Reduck extension.

### Does it change anything on miro.com, or only read data?

It only reads. It looks things up on miro.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/miro.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/miro.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/miro.com/download_invoice
