# Remove Castorama product from cart

Automatically remove Castorama product from cart on castorama.fr. Remove a product from the castorama.fr cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account.

- Site: castorama.fr
- Address: `reduck/castorama.fr/remove_from_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/castorama.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/castorama.fr/remove_from_cart
```

## Input

- `productId` (string, required): Product id of the line to remove, as returned by List Castorama cart items or Search Castorama products.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)
- `removed` (boolean, required)

## FAQ

### What does "Remove Castorama product from cart" do?

Remove a product from the castorama.fr cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account.

### How do I automatically remove Castorama product from cart on castorama.fr?

Ask an AI agent connected to Reduck to run reduck/castorama.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/castorama.fr/remove_from_cart

### Is there a castorama.fr API to remove Castorama product from cart?

You do not need one. "Remove Castorama product from cart" drives the real castorama.fr pages in a browser, so it works whether or not castorama.fr offers an API for this.

### What information do I need to provide?

Required: productId.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to castorama.fr?

No. It only uses pages of castorama.fr that are reachable without signing in.

### Does it change anything on castorama.fr, or only read data?

It makes changes on castorama.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/castorama.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/castorama.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/castorama.fr/remove_from_cart
