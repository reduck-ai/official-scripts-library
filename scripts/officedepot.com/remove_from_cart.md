# Remove Office Depot product from cart

Automatically remove Office Depot product from cart on officedepot.com. Remove a product from the OfficeDepot.com cart of this browser by its product id (the item number, as returned by List Office Depot cart items), whatever its quantity and on every line it sits on, and return what is left in the cart: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in US dollars, plus the item count and the subtotal. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account.

- Site: officedepot.com
- Address: `reduck/officedepot.com/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/officedepot.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/officedepot.com/remove_from_cart
```

## Input

- `product_id` (string, required): Office Depot item number of the product to remove: productId of List Office Depot cart items or Add Office Depot product to cart.

## Output

- `count` (integer, required): Number of units left in the cart.
- `lines` (array, required)
- `total` (number | null, required): Subtotal of the cart in US dollars, before tax and delivery.
- `removed` (boolean, required): True when the product was in the cart and is gone now; false when it was not in the cart.

## FAQ

### What does "Remove Office Depot product from cart" do?

Remove a product from the OfficeDepot.com cart of this browser by its product id (the item number, as returned by List Office Depot cart items), whatever its quantity and on every line it sits on, and return what is left in the cart: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in US dollars, plus the item count and the subtotal. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account.

### How do I automatically remove Office Depot product from cart on officedepot.com?

Ask an AI agent connected to Reduck to run reduck/officedepot.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/officedepot.com/remove_from_cart

### Is there a officedepot.com API to remove Office Depot product from cart?

You do not need one. "Remove Office Depot product from cart" drives the real officedepot.com pages in a browser, so it works whether or not officedepot.com offers an API for this.

### What information do I need to provide?

Required: product_id.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to officedepot.com?

No. It only uses pages of officedepot.com that are reachable without signing in.

### Does it change anything on officedepot.com, or only read data?

It makes changes on officedepot.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/officedepot.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/officedepot.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/officedepot.com/remove_from_cart
