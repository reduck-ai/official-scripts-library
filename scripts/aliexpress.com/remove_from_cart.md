# Remove AliExpress product from cart

Automatically remove AliExpress product from cart on aliexpress.com. Remove a product from the AliExpress cart of this browser by its product id (as List AliExpress cart items returns it), every variant and whatever the quantity, and return what is left in the cart: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price, plus the unit count and the total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account.

- Site: aliexpress.com
- Address: `reduck/aliexpress.com/remove_from_cart`
- Updated: 2026-11-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/aliexpress.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/remove_from_cart
```

## Input

- `product_id` (string, required): Product id of the lines to remove, as List AliExpress cart items or Add AliExpress product to cart return it (a product page link works too). Every line of this product is removed, whatever its variant and quantity.
- `review_hash` (string, optional): review_hash of each line of this product, from List AliExpress cart items, comma-separated. Without it, or when a line changed since, nothing is removed and the error gives the lines as they are now with their hashes.

## Output

- `count` (integer, required): Number of units left in the cart.
- `lines` (array, required)
- `total` (number | null, required): Sum of the line prices left, shipping not included.
- `removed` (boolean, required): True when the product was in the cart and is gone now; false when it was not in the cart.
- `currency` (string | null, optional)

## FAQ

### What does "Remove AliExpress product from cart" do?

Remove a product from the AliExpress cart of this browser by its product id (as List AliExpress cart items returns it), every variant and whatever the quantity, and return what is left in the cart: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price, plus the unit count and the total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account.

### How do I automatically remove AliExpress product from cart on aliexpress.com?

Ask an AI agent connected to Reduck to run reduck/aliexpress.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/remove_from_cart

### Is there a aliexpress.com API to remove AliExpress product from cart?

You do not need one. "Remove AliExpress product from cart" drives the real aliexpress.com pages in a browser, so it works whether or not aliexpress.com offers an API for this.

### What information do I need to provide?

Required: product_id. Optional: review_hash.

### What does it return?

It returns count, lines, total, removed, currency.

### Do I need to be logged in to aliexpress.com?

No. It only uses pages of aliexpress.com that are reachable without signing in.

### Does it change anything on aliexpress.com, or only read data?

It makes changes on aliexpress.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/aliexpress.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/aliexpress.com/remove_from_cart
