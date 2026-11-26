# Remove ManoMano product from cart

Automatically remove ManoMano product from cart on manomano.fr. Remove a product from the ManoMano.fr cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its product id, name, the seller that ships it, quantity, unit price and line price in euros, plus the item count and the total of the products. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account.

- Site: manomano.fr
- Address: `reduck/manomano.fr/remove_from_cart`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/manomano.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/manomano.fr/remove_from_cart
```

## Input

- `productId` (string, required): Product id of the cart line to remove, as returned by List ManoMano cart items or Add ManoMano product to cart.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required): Total of the products in euros, taxes included, delivery not included.
- `removed` (boolean, required)
- `productId` (string, required)

## FAQ

### What does "Remove ManoMano product from cart" do?

Remove a product from the ManoMano.fr cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its product id, name, the seller that ships it, quantity, unit price and line price in euros, plus the item count and the total of the products. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account.

### How do I automatically remove ManoMano product from cart on manomano.fr?

Ask an AI agent connected to Reduck to run reduck/manomano.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/manomano.fr/remove_from_cart

### Is there a manomano.fr API to remove ManoMano product from cart?

You do not need one. "Remove ManoMano product from cart" drives the real manomano.fr pages in a browser, so it works whether or not manomano.fr offers an API for this.

### What information do I need to provide?

Required: productId.

### What does it return?

It returns count, lines, total, removed, productId.

### Do I need to be logged in to manomano.fr?

No. It only uses pages of manomano.fr that are reachable without signing in.

### Does it change anything on manomano.fr, or only read data?

It makes changes on manomano.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/manomano.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/manomano.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/manomano.fr/remove_from_cart
