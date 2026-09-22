# Download PDF from a direct URL

Automatically download PDF from a direct URL on reduck.ai. Generic PDF/invoice downloader: given any direct, public tokenized PDF URL (Stripe pay.stripe.com/.../pdf, Orb assets.withorb.com, Chargify .pdf, etc.), downloads the file and returns path and filename. Works for public tokenized URLs only; PDFs gated behind a vendor session need that vendor's own download script.

- Site: reduck.ai
- Address: `reduck/reduck.ai/download_pdf_url`
- Updated: 2026-08-26 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reduck.ai/download_pdf_url`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reduck.ai/download_pdf_url
```

## Input

- `url` (string, required): Direct PDF URL (e.g. a pdfUrl from a list_invoices script).
- `filename` (string, optional): Preferred output filename. Honoured when the PDF is fetched in-page; a PDF the browser downloads natively keeps the name the server sends.

## Output

- `path` (string, required)
- `filename` (string, required)
- `via` (string, optional): How the bytes were captured: "native-download" or "in-page-fetch".
- `sourceUrl` (string, optional)

## FAQ

### What does "Download PDF from a direct URL" do?

Generic PDF/invoice downloader: given any direct, public tokenized PDF URL (Stripe pay.stripe.com/.../pdf, Orb assets.withorb.com, Chargify .pdf, etc.), downloads the file and returns path and filename. Works for public tokenized URLs only; PDFs gated behind a vendor session need that vendor's own download script.

### How do I automatically download PDF from a direct URL on reduck.ai?

Ask an AI agent connected to Reduck to run reduck/reduck.ai/download_pdf_url, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reduck.ai/download_pdf_url

### Is there a reduck.ai API to download PDF from a direct URL?

You do not need one. "Download PDF from a direct URL" drives the real reduck.ai pages in a browser, so it works whether or not reduck.ai offers an API for this.

### What information do I need to provide?

Required: url. Optional: filename.

### What does it return?

It returns via, path, filename, sourceUrl.

### Do I need to be logged in to reduck.ai?

No. It only uses pages of reduck.ai that are reachable without signing in.

### Does it change anything on reduck.ai, or only read data?

It only reads. It looks things up on reduck.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reduck.ai/download_pdf_url, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reduck.ai/download_pdf_url

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reduck.ai/download_pdf_url
