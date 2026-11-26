# Remove eBay item from cart

Automatically remove eBay item from cart on ebay.com. Remove an item from your eBay (ebay.com) cart by item id (and variation_id for a multi-variation listing), whatever its quantity, and return what is left in the cart (lines, item count, subtotal). An item that is not in the cart is reported as not present, and nothing is changed.

- Site: ebay.com
- Address: `reduck/ebay.com/remove_from_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ebay.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ebay.com/remove_from_cart
```

## Input

- `product_id` (string, required): eBay item id of the line to remove (productId from list_cart_items), or its listing link. Every line of the item goes, whatever the quantity.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)
- `removed` (boolean, required): False when the item was not in the cart; nothing was changed then.

## FAQ

### What does "Remove eBay item from cart" do?

Remove an item from your eBay (ebay.com) cart by item id (and variation_id for a multi-variation listing), whatever its quantity, and return what is left in the cart (lines, item count, subtotal). An item that is not in the cart is reported as not present, and nothing is changed.

### How do I automatically remove eBay item from cart on ebay.com?

Ask an AI agent connected to Reduck to run reduck/ebay.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/remove_from_cart

### Is there a ebay.com API to remove eBay item from cart?

You do not need one. "Remove eBay item from cart" drives the real ebay.com pages in a browser, so it works whether or not ebay.com offers an API for this.

### What information do I need to provide?

Required: product_id.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to ebay.com?

No. It only uses pages of ebay.com that are reachable without signing in.

### Does it change anything on ebay.com, or only read data?

It makes changes on ebay.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ebay.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/ebay.com/remove_from_cart
