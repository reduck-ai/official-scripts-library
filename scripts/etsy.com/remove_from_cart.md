# Remove Etsy listing from cart

Automatically remove Etsy listing from cart on etsy.com. Remove a listing from your Etsy (etsy.com) cart by listing id, every line of it or only one variation (inventory_id from list_cart_items), and return what is left in the cart. A listing that is not in the cart is reported as not present, and nothing is changed.

- Site: etsy.com
- Address: `reduck/etsy.com/remove_from_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/etsy.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/etsy.com/remove_from_cart
```

## Input

- `product_id` (string, required): Etsy listing id of the line to remove (productId from list_cart_items), or its listing link. Every line of the listing goes, whatever the quantity.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)
- `removed` (boolean, required): False when the listing was not in the cart; nothing was changed then.

## FAQ

### What does "Remove Etsy listing from cart" do?

Remove a listing from your Etsy (etsy.com) cart by listing id, every line of it or only one variation (inventory_id from list_cart_items), and return what is left in the cart. A listing that is not in the cart is reported as not present, and nothing is changed.

### How do I automatically remove Etsy listing from cart on etsy.com?

Ask an AI agent connected to Reduck to run reduck/etsy.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/etsy.com/remove_from_cart

### Is there a etsy.com API to remove Etsy listing from cart?

You do not need one. "Remove Etsy listing from cart" drives the real etsy.com pages in a browser, so it works whether or not etsy.com offers an API for this.

### What information do I need to provide?

Required: product_id.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to etsy.com?

No. It only uses pages of etsy.com that are reachable without signing in.

### Does it change anything on etsy.com, or only read data?

It makes changes on etsy.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/etsy.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/etsy.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/etsy.com/remove_from_cart
