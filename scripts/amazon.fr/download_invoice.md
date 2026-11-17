# Download Amazon.fr invoice

Automatically download Amazon.fr invoice on amazon.fr. Download one invoice PDF of an Amazon.fr order, by order number and invoice number (1 for the first invoice, as List Amazon.fr order invoices numbers them; an order shipped in parts or by several sellers can have several). Returns the saved file. Fails when the order has no invoice yet, or fewer invoices than the number asked.

- Site: amazon.fr
- Address: `reduck/amazon.fr/download_invoice`
- Updated: 2026-11-16 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.fr/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.fr/download_invoice
```

## Input

- `order_id` (string, required): The order number, for example 404-8237026-9000347, from List Amazon.fr order invoices.
- `invoice_number` (integer, optional): Which invoice of the order, from 1, as List Amazon.fr order invoices numbers them.

## Output

- `filename` (string, required)
- `order_id` (string, required)
- `invoice_number` (integer, required)
- `url` (string | null, optional)
- `path` (string | null, optional)
- `size_bytes` (integer, optional)
- `invoice_count` (integer, optional)

## FAQ

### What does "Download Amazon.fr invoice" do?

Download one invoice PDF of an Amazon.fr order, by order number and invoice number (1 for the first invoice, as List Amazon.fr order invoices numbers them; an order shipped in parts or by several sellers can have several). Returns the saved file. Fails when the order has no invoice yet, or fewer invoices than the number asked.

### How do I automatically download Amazon.fr invoice on amazon.fr?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/download_invoice

### Is there a amazon.fr API to download Amazon.fr invoice?

You do not need one. "Download Amazon.fr invoice" drives the real amazon.fr pages in a browser, so it works whether or not amazon.fr offers an API for this.

### What information do I need to provide?

Required: order_id. Optional: invoice_number.

### What does it return?

It returns url, path, filename, order_id, size_bytes, invoice_count, invoice_number.

### Do I need to be logged in to amazon.fr?

Yes. It acts as you on amazon.fr: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the amazon.fr cookies saved by the Reduck extension.

### Does it change anything on amazon.fr, or only read data?

It only reads. It looks things up on amazon.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.fr/download_invoice
