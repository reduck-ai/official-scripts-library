# List Amazon.fr order invoices

Automatically list Amazon.fr order invoices on amazon.fr. List the orders of your Amazon.fr account for a period, 10 per page, each with its date, total, item titles and its invoices, numbered from 1. Download Amazon.fr invoice takes the order number and that invoice number. Each invoice's link is only valid for a short time; it is not a stable id. An order with no invoice yet (not shipped, a digital order, or a seller that issues none) returns an empty invoices list; invoice_menu says whether Amazon offered an invoice menu for it at all. A period with no orders returns an empty list.

- Site: amazon.fr
- Address: `reduck/amazon.fr/list_invoices`
- Updated: 2026-11-16 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.fr/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.fr/list_invoices
```

## Input

- `page` (integer, optional): Page of 10 orders, from 1.
- `time_filter` (string, optional): The period of Your Orders: last30, months-3, or year-YYYY (for example year-2026).

## Output

- `orders` (array, required)
- `has_next_page` (boolean, required)
- `page` (integer, optional)
- `time_filter` (string, optional)

## FAQ

### What does "List Amazon.fr order invoices" do?

List the orders of your Amazon.fr account for a period, 10 per page, each with its date, total, item titles and its invoices, numbered from 1. Download Amazon.fr invoice takes the order number and that invoice number. Each invoice's link is only valid for a short time; it is not a stable id. An order with no invoice yet (not shipped, a digital order, or a seller that issues none) returns an empty invoices list; invoice_menu says whether Amazon offered an invoice menu for it at all. A period with no orders returns an empty list.

### How do I automatically list Amazon.fr order invoices on amazon.fr?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/list_invoices

### Is there a amazon.fr API to list Amazon.fr order invoices?

You do not need one. "List Amazon.fr order invoices" drives the real amazon.fr pages in a browser, so it works whether or not amazon.fr offers an API for this.

### What information do I need to provide?

Optional: page, time_filter.

### What does it return?

It returns page, orders, time_filter, has_next_page.

### Do I need to be logged in to amazon.fr?

Yes. It acts as you on amazon.fr: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the amazon.fr cookies saved by the Reduck extension.

### Does it change anything on amazon.fr, or only read data?

It only reads. It looks things up on amazon.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.fr/list_invoices
