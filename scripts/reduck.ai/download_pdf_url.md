# Download PDF from a direct URL

Automatically download PDF from a direct URL on reduck.ai. Download a PDF from a direct, public link (for example an invoice PDF link that a list_invoices script returns) and return the saved file name with its path on your computer, or a download link when it runs on a managed browser. Links that only work in a signed-in vendor session need that vendor's own download script. A link that opens in the browser instead of downloading, on a site with no page of its own to fetch it from, fails with an error that says so.

- Site: reduck.ai
- Address: `reduck/reduck.ai/download_pdf_url`
- Updated: 2026-10-22 (v7)
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

- `filename` (string, required): The saved file name; it can end in " (2)" when a file of that name already exists.
- `url` (string | null, optional): A link to the saved file on a managed browser; null on the user's Chrome.
- `via` (string, optional): How the bytes were captured: "native-download" or "in-page-fetch".
- `path` (string | null, optional): The saved file on the machine that runs the browser (the user's Chrome); null on a managed browser.
- `sourceUrl` (string, optional)

## FAQ

### What does "Download PDF from a direct URL" do?

Download a PDF from a direct, public link (for example an invoice PDF link that a list_invoices script returns) and return the saved file name with its path on your computer, or a download link when it runs on a managed browser. Links that only work in a signed-in vendor session need that vendor's own download script. A link that opens in the browser instead of downloading, on a site with no page of its own to fetch it from, fails with an error that says so.

### How do I automatically download PDF from a direct URL on reduck.ai?

Ask an AI agent connected to Reduck to run reduck/reduck.ai/download_pdf_url, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reduck.ai/download_pdf_url

### Is there a reduck.ai API to download PDF from a direct URL?

You do not need one. "Download PDF from a direct URL" drives the real reduck.ai pages in a browser, so it works whether or not reduck.ai offers an API for this.

### What information do I need to provide?

Required: url. Optional: filename.

### What does it return?

It returns url, via, path, filename, sourceUrl.

### Do I need to be logged in to reduck.ai?

No. It only uses pages of reduck.ai that are reachable without signing in.

### Does it change anything on reduck.ai, or only read data?

It only reads. It looks things up on reduck.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reduck.ai/download_pdf_url, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reduck.ai/download_pdf_url

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/reduck.ai/download_pdf_url
