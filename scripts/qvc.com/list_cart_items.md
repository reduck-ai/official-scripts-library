# List QVC cart items

Automatically list QVC cart items on qvc.com. List the lines of the QVC cart of this browser, with quantities, prices and the merchandise subtotal.

- Site: qvc.com
- Address: `reduck/qvc.com/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/qvc.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/qvc.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Merchandise subtotal in USD, without tax and shipping.

## FAQ

### What does "List QVC cart items" do?

List the lines of the QVC cart of this browser, with quantities, prices and the merchandise subtotal.

### How do I automatically list QVC cart items on qvc.com?

Ask an AI agent connected to Reduck to run reduck/qvc.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/qvc.com/list_cart_items

### Is there a qvc.com API to list QVC cart items?

You do not need one. "List QVC cart items" drives the real qvc.com pages in a browser, so it works whether or not qvc.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to qvc.com?

No. It only uses pages of qvc.com that are reachable without signing in.

### Does it change anything on qvc.com, or only read data?

It only reads. It looks things up on qvc.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/qvc.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/qvc.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/qvc.com/list_cart_items
