# Remove from Alibaba.com cart

Automatically remove from Alibaba.com cart on alibaba.com. Remove a product from this browser's Alibaba.com cart by product id, whatever its quantity, as the cart page's remove button does: all its variants, or only one when a variant id is given. Returns removed and the cart as it is after the removal, in the shape List Alibaba.com cart items gives. A product or variant that is not in the cart is reported with removed false and the cart unchanged, not as a failure. The cart works without sign-in.

- Site: alibaba.com
- Address: `reduck/alibaba.com/remove_from_cart`
- Updated: 2026-11-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/alibaba.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/alibaba.com/remove_from_cart
```

## Input

- `product_id` (string, required): Alibaba.com product id of the cart line, as List Alibaba.com cart items gives it, or a product page link.
- `variant_id` (string, optional): Remove only this variant of the product (the offerId of List Alibaba.com cart items). Without it, every variant of the product is removed, whatever its quantity.

## Output

- `count` (integer, required): Number of items in the cart after the removal.
- `lines` (array, required): The cart's lines after the removal, one per product variant.
- `total` (number | null, required): Item subtotal of the cart after the removal, in the display currency, shipping not included. 0 for an empty cart.
- `removed` (boolean, required): False when the product was not in the cart; nothing was changed then.

## FAQ

### What does "Remove from Alibaba.com cart" do?

Remove a product from this browser's Alibaba.com cart by product id, whatever its quantity, as the cart page's remove button does: all its variants, or only one when a variant id is given. Returns removed and the cart as it is after the removal, in the shape List Alibaba.com cart items gives. A product or variant that is not in the cart is reported with removed false and the cart unchanged, not as a failure. The cart works without sign-in.

### How do I automatically remove from Alibaba.com cart on alibaba.com?

Ask an AI agent connected to Reduck to run reduck/alibaba.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alibaba.com/remove_from_cart

### Is there a alibaba.com API to remove from Alibaba.com cart?

You do not need one. "Remove from Alibaba.com cart" drives the real alibaba.com pages in a browser, so it works whether or not alibaba.com offers an API for this.

### What information do I need to provide?

Required: product_id. Optional: variant_id.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to alibaba.com?

No. It only uses pages of alibaba.com that are reachable without signing in.

### Does it change anything on alibaba.com, or only read data?

It makes changes on alibaba.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/alibaba.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alibaba.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/alibaba.com/remove_from_cart
