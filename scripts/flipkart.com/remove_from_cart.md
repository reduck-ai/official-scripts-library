# Remove a product from the Flipkart cart

Automatically remove a product from the Flipkart cart on flipkart.com. Remove a product from the Flipkart India (flipkart.com) cart of this browser, by offer id (one seller's listing, as List the items in the Flipkart cart gives it) or by product id (every line of that product). Returns whether something was removed and the whole cart afterwards: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in Indian rupees, the item count and the total amount. A product that is not in the cart gives removed false and changes nothing. Works as a guest, with no account.

- Site: flipkart.com
- Address: `reduck/flipkart.com/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/flipkart.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/flipkart.com/remove_from_cart
```

## Input

- `offer_id` (string, optional): Offer id of the cart line, the offerId of List the items in the Flipkart cart.
- `product_id` (string, optional): Flipkart product id: every cart line of this product is removed. Used when no offer_id is given.

## Output

- `count` (integer, required): Number of items left in the cart.
- `lines` (array, required)
- `total` (number | null, required): Total amount Flipkart shows for the cart, in rupees, with the platform fee.
- `removed` (boolean, required): True when at least one line was removed; false when the product was not in the cart.
- `currency` (string, required)

## FAQ

### What does "Remove a product from the Flipkart cart" do?

Remove a product from the Flipkart India (flipkart.com) cart of this browser, by offer id (one seller's listing, as List the items in the Flipkart cart gives it) or by product id (every line of that product). Returns whether something was removed and the whole cart afterwards: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in Indian rupees, the item count and the total amount. A product that is not in the cart gives removed false and changes nothing. Works as a guest, with no account.

### How do I automatically remove a product from the Flipkart cart on flipkart.com?

Ask an AI agent connected to Reduck to run reduck/flipkart.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/flipkart.com/remove_from_cart

### Is there a flipkart.com API to remove a product from the Flipkart cart?

You do not need one. "Remove a product from the Flipkart cart" drives the real flipkart.com pages in a browser, so it works whether or not flipkart.com offers an API for this.

### What information do I need to provide?

Optional: offer_id, product_id.

### What does it return?

It returns count, lines, total, removed, currency.

### Do I need to be logged in to flipkart.com?

No. It only uses pages of flipkart.com that are reachable without signing in.

### Does it change anything on flipkart.com, or only read data?

It makes changes on flipkart.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/flipkart.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/flipkart.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/flipkart.com/remove_from_cart
