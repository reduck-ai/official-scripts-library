# List Miro invoices

Automatically list Miro invoices on miro.com. List Miro company billing invoices. Returns total plus invoices (id, date, description, amount, status, pdfUrl) — metadata only, with dates as ISO YYYY-MM-DD and amounts with their ISO currency, e.g. "10.00 EUR". Feed a row's pdfUrl to miro.com/download_invoice to fetch that invoice's PDF. Only a company or team billing admin can see billing; a personal account with no organization is reported as such rather than timing out.

- Site: miro.com
- Address: `reduck/miro.com/list_invoices`
- Updated: 2026-08-21 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/miro.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/miro.com/list_invoices
```

## Input

It takes no input.

## Output

- `total` (integer, required)
- `invoices` (array, required)

## FAQ

### What does "List Miro invoices" do?

List Miro company billing invoices. Returns total plus invoices (id, date, description, amount, status, pdfUrl) — metadata only, with dates as ISO YYYY-MM-DD and amounts with their ISO currency, e.g. "10.00 EUR". Feed a row's pdfUrl to miro.com/download_invoice to fetch that invoice's PDF. Only a company or team billing admin can see billing; a personal account with no organization is reported as such rather than timing out.

### How do I automatically list Miro invoices on miro.com?

Ask an AI agent connected to Reduck to run reduck/miro.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/miro.com/list_invoices

### Is there a miro.com API to list Miro invoices?

You do not need one. "List Miro invoices" drives the real miro.com pages in a browser, so it works whether or not miro.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, invoices.

### Do I need to be logged in to miro.com?

Yes. It acts as you on miro.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the miro.com cookies saved by the Reduck extension.

### Does it change anything on miro.com, or only read data?

It only reads. It looks things up on miro.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/miro.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/miro.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/miro.com/list_invoices
