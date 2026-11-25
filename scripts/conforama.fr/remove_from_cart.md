# Remove product from Conforama cart

Automatically remove product from Conforama cart on conforama.fr. Remove a product from the Conforama cart of this browser by its product id or product page link, whatever its quantity, and return what is left in the cart: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. When the same product is in the cart from several sellers, pass the offer id to pick the line. Works as a guest, with no account.

- Site: conforama.fr
- Address: `reduck/conforama.fr/remove_from_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/conforama.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/conforama.fr/remove_from_cart
```

## Input

- `product` (string, required): Product id such as 769466, or the link of its Conforama product page, as returned by Search Conforama products or Add Conforama product to cart.
- `offerId` (string, optional): Marketplace offer id of the line, only needed when the same product is in the cart from several sellers.

## Output

- `count` (integer, required): Units left in the cart.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros after the removal.
- `removed` (boolean, required): False when the product was not in the cart.
- `productId` (string, required)

## FAQ

### What does "Remove product from Conforama cart" do?

Remove a product from the Conforama cart of this browser by its product id or product page link, whatever its quantity, and return what is left in the cart: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. When the same product is in the cart from several sellers, pass the offer id to pick the line. Works as a guest, with no account.

### How do I automatically remove product from Conforama cart on conforama.fr?

Ask an AI agent connected to Reduck to run reduck/conforama.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conforama.fr/remove_from_cart

### Is there a conforama.fr API to remove product from Conforama cart?

You do not need one. "Remove product from Conforama cart" drives the real conforama.fr pages in a browser, so it works whether or not conforama.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: offerId.

### What does it return?

It returns count, lines, total, removed, productId.

### Do I need to be logged in to conforama.fr?

No. It only uses pages of conforama.fr that are reachable without signing in.

### Does it change anything on conforama.fr, or only read data?

It makes changes on conforama.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/conforama.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conforama.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/conforama.fr/remove_from_cart
