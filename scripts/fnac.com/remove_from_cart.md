# Remove a product from the Fnac cart

Automatically remove a product from the Fnac cart on fnac.com. Remove a product from the Fnac.com cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. When the same product is in the cart from several sellers, pass the offer id to pick the line.

- Site: fnac.com
- Address: `reduck/fnac.com/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/fnac.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/fnac.com/remove_from_cart
```

## Input

- `product` (string, required): Product id as the cart lists it (the digits), or as Search Fnac products returns it (a<number> or mp<number>), or a www.fnac.com product page link.
- `offer_id` (string | null, optional): Offer id of the cart line, only needed when the same product is in the cart from several sellers.
- `review_hash` (string, optional): review_hash of the line, from List the Fnac cart items. Without it, or when the line changed since, nothing is removed and the error gives the line as it is now and its hash.

## Output

- `count` (integer, required): Number of items left in the cart, quantities summed.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros as the site states it.
- `removed` (boolean, required)

## FAQ

### What does "Remove a product from the Fnac cart" do?

Remove a product from the Fnac.com cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. When the same product is in the cart from several sellers, pass the offer id to pick the line.

### How do I automatically remove a product from the Fnac cart on fnac.com?

Ask an AI agent connected to Reduck to run reduck/fnac.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/fnac.com/remove_from_cart

### Is there a fnac.com API to remove a product from the Fnac cart?

You do not need one. "Remove a product from the Fnac cart" drives the real fnac.com pages in a browser, so it works whether or not fnac.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: offer_id, review_hash.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to fnac.com?

No. It only uses pages of fnac.com that are reachable without signing in.

### Does it change anything on fnac.com, or only read data?

It makes changes on fnac.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/fnac.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/fnac.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/fnac.com/remove_from_cart
