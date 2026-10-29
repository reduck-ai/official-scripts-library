# Download a Miro invoice PDF

Automatically download a Miro invoice PDF on miro.com. Download one Miro billing invoice PDF, given the pdfUrl that miro.com/list_invoices returns (listing invoices needs a Miro sign-in; the download itself does not). Returns the saved filename plus where to get the file: a path in the Downloads folder on your own Chrome, or a url on a managed browser. The filename can end in " (2)" when the same invoice was saved before. Invoice links expire: an expired one fails with a message to fetch a fresh pdfUrl from list_invoices.

- Site: miro.com
- Address: `reduck/miro.com/download_invoice`
- Updated: 2026-10-28 (v6)
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

- `url` (string | null, required): Where to fetch the PDF when the run used a managed browser. Null on the user's own Chrome, which returns path instead.
- `path` (string | null, required): Where the PDF was saved in the Downloads folder of the user's own Chrome. Null on a managed browser, which returns url instead.
- `filename` (string, required): The invoice's file name, as saved (e.g. Invoice-EB7Y9VN8-0001.pdf).

## FAQ

### What does "Download a Miro invoice PDF" do?

Download one Miro billing invoice PDF, given the pdfUrl that miro.com/list_invoices returns (listing invoices needs a Miro sign-in; the download itself does not). Returns the saved filename plus where to get the file: a path in the Downloads folder on your own Chrome, or a url on a managed browser. The filename can end in " (2)" when the same invoice was saved before. Invoice links expire: an expired one fails with a message to fetch a fresh pdfUrl from list_invoices.

### How do I automatically download a Miro invoice PDF on miro.com?

Ask an AI agent connected to Reduck to run reduck/miro.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/miro.com/download_invoice

### Is there a miro.com API to download a Miro invoice PDF?

You do not need one. "Download a Miro invoice PDF" drives the real miro.com pages in a browser, so it works whether or not miro.com offers an API for this.

### What information do I need to provide?

Required: pdfUrl. Optional: id.

### What does it return?

It returns url, path, filename.

### Do I need to be logged in to miro.com?

No. It only uses pages of miro.com that are reachable without signing in.

### Does it change anything on miro.com, or only read data?

It only reads. It looks things up on miro.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/miro.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/miro.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/miro.com/download_invoice
