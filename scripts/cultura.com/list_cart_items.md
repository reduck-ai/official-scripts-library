# List Cultura cart items

Automatically list Cultura cart items on cultura.com. List the products in the cultura.com basket.

- Site: cultura.com
- Address: `reduck/cultura.com/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cultura.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cultura.com/list_cart_items
```

## Input

It takes no input.

## Output

- `items` (array, required)
- `total` (number | null, required): Basket subtotal including tax, before delivery
- `currency` (string, required)
- `item_count` (integer, required)

## FAQ

### What does "List Cultura cart items" do?

List the products in the cultura.com basket.

### How do I automatically list Cultura cart items on cultura.com?

Ask an AI agent connected to Reduck to run reduck/cultura.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cultura.com/list_cart_items

### Is there a cultura.com API to list Cultura cart items?

You do not need one. "List Cultura cart items" drives the real cultura.com pages in a browser, so it works whether or not cultura.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns items, total, currency, item_count.

### Do I need to be logged in to cultura.com?

No. It only uses pages of cultura.com that are reachable without signing in.

### Does it change anything on cultura.com, or only read data?

It only reads. It looks things up on cultura.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cultura.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cultura.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/cultura.com/list_cart_items
