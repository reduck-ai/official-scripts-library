# List Uber Eats orders

Automatically list Uber Eats orders on ubereats.com. List past Uber Eats orders with their detail. Returns total and orders (date, restaurant, items, total, itemCount, orderId, hasInvoice, pdfUrl); pdfUrl is only present for orders that have a receipt (hasInvoice true).

- Site: ubereats.com
- Address: `reduck/ubereats.com/list_orders`
- Updated: 2026-08-27 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ubereats.com/list_orders`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ubereats.com/list_orders
```

## Input

It takes no input.

## Output

- `total` (integer, required)
- `orders` (array, required)

## FAQ

### What does "List Uber Eats orders" do?

List past Uber Eats orders with their detail. Returns total and orders (date, restaurant, items, total, itemCount, orderId, hasInvoice, pdfUrl); pdfUrl is only present for orders that have a receipt (hasInvoice true).

### How do I automatically list Uber Eats orders on ubereats.com?

Ask an AI agent connected to Reduck to run reduck/ubereats.com/list_orders, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ubereats.com/list_orders

### Is there a ubereats.com API to list Uber Eats orders?

You do not need one. "List Uber Eats orders" drives the real ubereats.com pages in a browser, so it works whether or not ubereats.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, orders.

### Do I need to be logged in to ubereats.com?

Yes. It acts as you on ubereats.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the ubereats.com cookies saved by the Reduck extension.

### Does it change anything on ubereats.com, or only read data?

It only reads. It looks things up on ubereats.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ubereats.com/list_orders, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ubereats.com/list_orders

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ubereats.com/list_orders
