# Remove from Best Buy cart

Automatically remove from Best Buy cart on bestbuy.com. Remove a product from this browser's Best Buy (US) cart by SKU, whatever its quantity, and return the cart as it is after the removal, in the shape List Best Buy cart items gives, with removed true. A SKU that is not in the cart is reported with removed false and the cart unchanged, not as a failure.

- Site: bestbuy.com
- Address: `reduck/bestbuy.com/remove_from_cart`
- Updated: 2026-11-17 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bestbuy.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/remove_from_cart
```

## Input

- `sku` (string, required): Best Buy SKU of the cart item, as List Best Buy cart items gives it.

## Output

- `sku` (string, required)
- `items` (array, required)
- `removed` (boolean, required): False when the SKU was not in the cart.
- `summary` (object | null, required)
- `item_count` (integer, required)

## FAQ

### What does "Remove from Best Buy cart" do?

Remove a product from this browser's Best Buy (US) cart by SKU, whatever its quantity, and return the cart as it is after the removal, in the shape List Best Buy cart items gives, with removed true. A SKU that is not in the cart is reported with removed false and the cart unchanged, not as a failure.

### How do I automatically remove from Best Buy cart on bestbuy.com?

Ask an AI agent connected to Reduck to run reduck/bestbuy.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/remove_from_cart

### Is there a bestbuy.com API to remove from Best Buy cart?

You do not need one. "Remove from Best Buy cart" drives the real bestbuy.com pages in a browser, so it works whether or not bestbuy.com offers an API for this.

### What information do I need to provide?

Required: sku.

### What does it return?

It returns sku, items, removed, summary, item_count.

### Do I need to be logged in to bestbuy.com?

No. It only uses pages of bestbuy.com that are reachable without signing in.

### Does it change anything on bestbuy.com, or only read data?

It makes changes on bestbuy.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bestbuy.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/remove_from_cart

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/bestbuy.com/remove_from_cart
