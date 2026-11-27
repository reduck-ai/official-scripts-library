# Remove from Container Store cart

Automatically remove from Container Store cart on containerstore.com. Remove a product of The Container Store (containerstore.com, US) from the cart of this browser, by product id or link, whatever its quantity: every line of it, or only the line of one variant when its SKU id is given. Returns the cart after the removal and removed true. A product that is not in the cart leaves the cart unchanged and gives removed false, not an error.

- Site: containerstore.com
- Address: `reduck/containerstore.com/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/containerstore.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/containerstore.com/remove_from_cart
```

## Input

- `product` (string, required): Product id (the productId in a product link, for example 10022942), as List Container Store cart items gives it, or the product link.
- `variant` (string, optional): Optional. Variant (SKU) id: the offerId of the line in List Container Store cart items. Removes only that line.

## Output

- `count` (integer, required): Number of units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Order subtotal in USD as the cart shows it: before offers, shipping and tax.
- `removed` (boolean, required): False when the product was not in the cart.

## FAQ

### What does "Remove from Container Store cart" do?

Remove a product of The Container Store (containerstore.com, US) from the cart of this browser, by product id or link, whatever its quantity: every line of it, or only the line of one variant when its SKU id is given. Returns the cart after the removal and removed true. A product that is not in the cart leaves the cart unchanged and gives removed false, not an error.

### How do I automatically remove from Container Store cart on containerstore.com?

Ask an AI agent connected to Reduck to run reduck/containerstore.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/containerstore.com/remove_from_cart

### Is there a containerstore.com API to remove from Container Store cart?

You do not need one. "Remove from Container Store cart" drives the real containerstore.com pages in a browser, so it works whether or not containerstore.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: variant.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to containerstore.com?

No. It only uses pages of containerstore.com that are reachable without signing in.

### Does it change anything on containerstore.com, or only read data?

It makes changes on containerstore.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/containerstore.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/containerstore.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/containerstore.com/remove_from_cart
