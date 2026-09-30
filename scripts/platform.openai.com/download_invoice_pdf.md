# OpenAI API: download an OpenAI API platform invoice PDF

Automatically download an OpenAI API platform invoice PDF on platform.openai.com. An unofficial OpenAI API to download platform billing invoice PDFs. Download a billing invoice PDF from the signed-in OpenAI API platform organization (platform.openai.com; API usage and credits, not the ChatGPT subscription). Pass the invoice id (in_...) or number (e.g. PFWBT7SS-0003) as shown by list_invoices, or omit it for the most recent invoice. If OpenAI asks which API organization to use, it picks the one named in organization, or else the first offered. Returns the invoice number, status, total (cents), created date, and where the PDF was saved, plus every invoice number on the organization. It fails with the list of available invoices if the requested one does not exist. Read-only.

- Site: platform.openai.com
- Address: `reduck/platform.openai.com/download_invoice_pdf`
- Updated: 2026-09-29 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/platform.openai.com/download_invoice_pdf`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/platform.openai.com/download_invoice_pdf
```

## Input

- `invoice` (string, optional): Invoice id (in_...) or invoice number (e.g. PFWBT7SS-0003) as listed by list_invoices. Omit for the most recent invoice.
- `organization` (string, optional): Which API organization to use if OpenAI asks you to choose one (its name as shown). Defaults to the first one offered.

## Output

- `id` (string, required)
- `filename` (string | null, required)
- `url` (string | null, optional)
- `path` (string | null, optional): Where the PDF was saved on the machine running the browser.
- `total` (number | null, optional): Amount in the smallest currency unit (cents).
- `number` (string | null, optional)
- `status` (string | null, optional)
- `created` (string | null, optional)
- `currency` (string | null, optional)
- `available` (array, optional): All invoice numbers on the organization, newest first.

## FAQ

### What does "OpenAI API: download an OpenAI API platform invoice PDF" do?

An unofficial OpenAI API to download platform billing invoice PDFs. Download a billing invoice PDF from the signed-in OpenAI API platform organization (platform.openai.com; API usage and credits, not the ChatGPT subscription). Pass the invoice id (in_...) or number (e.g. PFWBT7SS-0003) as shown by list_invoices, or omit it for the most recent invoice. If OpenAI asks which API organization to use, it picks the one named in organization, or else the first offered. Returns the invoice number, status, total (cents), created date, and where the PDF was saved, plus every invoice number on the organization. It fails with the list of available invoices if the requested one does not exist. Read-only.

### How do I automatically download an OpenAI API platform invoice PDF on platform.openai.com?

Ask an AI agent connected to Reduck to run reduck/platform.openai.com/download_invoice_pdf, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/platform.openai.com/download_invoice_pdf

### Is there a platform.openai.com API to download an OpenAI API platform invoice PDF?

You do not need one. "OpenAI API: download an OpenAI API platform invoice PDF" drives the real platform.openai.com pages in a browser, so it works whether or not platform.openai.com offers an API for this.

### What information do I need to provide?

Optional: invoice, organization.

### What does it return?

It returns id, url, path, total, number, status, created, currency, filename, available.

### Do I need to be logged in to platform.openai.com?

Yes. It acts as you on platform.openai.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the platform.openai.com cookies saved by the Reduck extension.

### Does it change anything on platform.openai.com, or only read data?

It only reads. It looks things up on platform.openai.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/platform.openai.com/download_invoice_pdf, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/platform.openai.com/download_invoice_pdf

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/platform.openai.com/download_invoice_pdf
