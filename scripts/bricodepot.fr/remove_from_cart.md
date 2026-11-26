# Remove product from Brico Depot cart

Automatically remove product from Brico Depot cart on bricodepot.fr. Remove a product from the Brico Depot (bricodepot.fr) shopping cart of this browser by its product id (the sku that List Brico Depot cart items returns) or its product page link, whatever its quantity, and return what is left in the cart: the item count, the items total in euros (taxes included) and each line with its line id, product id, offer id, name, seller, quantity, unit price and line price. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account.

- Site: bricodepot.fr
- Address: `reduck/bricodepot.fr/remove_from_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bricodepot.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/remove_from_cart
```

## Input

- `product_id` (string, required): Product id of the line to remove: the productId of List Brico Depot cart items (a sku, for example 5063022538369), or the product page link.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Items total in euros, taxes included, delivery not included.
- `removed` (boolean, required): False when the product was not in the cart.

## FAQ

### What does "Remove product from Brico Depot cart" do?

Remove a product from the Brico Depot (bricodepot.fr) shopping cart of this browser by its product id (the sku that List Brico Depot cart items returns) or its product page link, whatever its quantity, and return what is left in the cart: the item count, the items total in euros (taxes included) and each line with its line id, product id, offer id, name, seller, quantity, unit price and line price. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account.

### How do I automatically remove product from Brico Depot cart on bricodepot.fr?

Ask an AI agent connected to Reduck to run reduck/bricodepot.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/remove_from_cart

### Is there a bricodepot.fr API to remove product from Brico Depot cart?

You do not need one. "Remove product from Brico Depot cart" drives the real bricodepot.fr pages in a browser, so it works whether or not bricodepot.fr offers an API for this.

### What information do I need to provide?

Required: product_id.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to bricodepot.fr?

No. It only uses pages of bricodepot.fr that are reachable without signing in.

### Does it change anything on bricodepot.fr, or only read data?

It makes changes on bricodepot.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bricodepot.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bricodepot.fr/remove_from_cart
