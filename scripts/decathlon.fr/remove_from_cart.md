# Remove Decathlon product from cart

Automatically remove Decathlon product from cart on decathlon.fr. Remove a product from the Decathlon.fr cart of this browser by its product id (the sku id of the exact size, as returned by List Decathlon cart items), whatever its quantity, and return what is left in the cart: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and the total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account.

- Site: decathlon.fr
- Address: `reduck/decathlon.fr/remove_from_cart`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/decathlon.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/decathlon.fr/remove_from_cart
```

## Input

- `product_id` (string, required): Product id of the line to remove: the sku id of the size, as returned by List Decathlon cart items or Add Decathlon product to cart.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)
- `removed` (boolean, required)

## FAQ

### What does "Remove Decathlon product from cart" do?

Remove a product from the Decathlon.fr cart of this browser by its product id (the sku id of the exact size, as returned by List Decathlon cart items), whatever its quantity, and return what is left in the cart: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and the total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account.

### How do I automatically remove Decathlon product from cart on decathlon.fr?

Ask an AI agent connected to Reduck to run reduck/decathlon.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/decathlon.fr/remove_from_cart

### Is there a decathlon.fr API to remove Decathlon product from cart?

You do not need one. "Remove Decathlon product from cart" drives the real decathlon.fr pages in a browser, so it works whether or not decathlon.fr offers an API for this.

### What information do I need to provide?

Required: product_id.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to decathlon.fr?

No. It only uses pages of decathlon.fr that are reachable without signing in.

### Does it change anything on decathlon.fr, or only read data?

It makes changes on decathlon.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/decathlon.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/decathlon.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/decathlon.fr/remove_from_cart
