# Adobe — list orders and invoices

Automatically list orders and invoices on adobe.com. List the orders / invoices and open quotes on the signed-in Adobe account (Account → Orders and invoices). Read-only; signed out is a clear error. An account with no purchases returns empty lists.

- Site: adobe.com
- Address: `reduck/adobe.com/list_orders`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/adobe.com/list_orders`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/adobe.com/list_orders
```

## Input

It takes no input.

## Output

- `orders` (array, required): Orders / invoices as Adobe's billing service returns them.
- `quotes` (array, required)
- `userId` (string | null, required)
- `orderCount` (integer, optional)
- `quoteCount` (integer, optional)

## FAQ

### What does "Adobe — list orders and invoices" do?

List the orders / invoices and open quotes on the signed-in Adobe account (Account → Orders and invoices). Read-only; signed out is a clear error. An account with no purchases returns empty lists.

### How do I automatically list orders and invoices on adobe.com?

Ask an AI agent connected to Reduck to run reduck/adobe.com/list_orders, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/adobe.com/list_orders

### Is there a adobe.com API to list orders and invoices?

You do not need one. "Adobe — list orders and invoices" drives the real adobe.com pages in a browser, so it works whether or not adobe.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns orders, quotes, userId, orderCount, quoteCount.

### Do I need to be logged in to adobe.com?

Yes. It acts as you on adobe.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the adobe.com cookies saved by the Reduck extension.

### Does it change anything on adobe.com, or only read data?

It only reads. It looks things up on adobe.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/adobe.com/list_orders, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/adobe.com/list_orders

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/adobe.com/list_orders
