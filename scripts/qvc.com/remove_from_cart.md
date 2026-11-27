# Remove a product from the QVC cart

Automatically remove a product from the QVC cart on qvc.com. Remove a product from the QVC cart of this browser, all its lines and units, and return the cart. A product that is not in the cart leaves the cart as it is.

- Site: qvc.com
- Address: `reduck/qvc.com/remove_from_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/qvc.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/qvc.com/remove_from_cart
```

## Input

- `product_id` (string, required): QVC item number (e.g. K316571) or a QVC product page link.

## Output

- `count` (integer, required): Number of units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Merchandise subtotal in USD, without tax and shipping.
- `removed` (boolean, required): False when the product was not in the cart.

## FAQ

### What does "Remove a product from the QVC cart" do?

Remove a product from the QVC cart of this browser, all its lines and units, and return the cart. A product that is not in the cart leaves the cart as it is.

### How do I automatically remove a product from the QVC cart on qvc.com?

Ask an AI agent connected to Reduck to run reduck/qvc.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/qvc.com/remove_from_cart

### Is there a qvc.com API to remove a product from the QVC cart?

You do not need one. "Remove a product from the QVC cart" drives the real qvc.com pages in a browser, so it works whether or not qvc.com offers an API for this.

### What information do I need to provide?

Required: product_id.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to qvc.com?

No. It only uses pages of qvc.com that are reachable without signing in.

### Does it change anything on qvc.com, or only read data?

It makes changes on qvc.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/qvc.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/qvc.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/qvc.com/remove_from_cart
