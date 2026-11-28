# Remove a product from the Samsung cart

Automatically remove a product from the Samsung cart on samsung.com. Remove a product from the Samsung US store (samsung.com/us) cart of this browser by its product id (the model code, as returned by List Samsung cart items), whatever its quantity and on every line it sits on, and return what is left in the cart: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in US dollars, plus the item count and the subtotal. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account.

- Site: samsung.com
- Address: `reduck/samsung.com/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/samsung.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/samsung.com/remove_from_cart
```

## Input

- `product_id` (string, required): Model code (SKU) of the product to remove: productId of List Samsung cart items or Add a product to the Samsung cart.

## Output

- `count` (integer, required): Number of units left in the cart.
- `lines` (array, required)
- `total` (number | null, required): Subtotal of the cart in US dollars, before tax and delivery.
- `removed` (boolean, required): True when the product was in the cart and is gone now; false when it was not in the cart.

## FAQ

### What does "Remove a product from the Samsung cart" do?

Remove a product from the Samsung US store (samsung.com/us) cart of this browser by its product id (the model code, as returned by List Samsung cart items), whatever its quantity and on every line it sits on, and return what is left in the cart: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in US dollars, plus the item count and the subtotal. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account.

### How do I automatically remove a product from the Samsung cart on samsung.com?

Ask an AI agent connected to Reduck to run reduck/samsung.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsung.com/remove_from_cart

### Is there a samsung.com API to remove a product from the Samsung cart?

You do not need one. "Remove a product from the Samsung cart" drives the real samsung.com pages in a browser, so it works whether or not samsung.com offers an API for this.

### What information do I need to provide?

Required: product_id.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to samsung.com?

No. It only uses pages of samsung.com that are reachable without signing in.

### Does it change anything on samsung.com, or only read data?

It makes changes on samsung.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/samsung.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsung.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/samsung.com/remove_from_cart
