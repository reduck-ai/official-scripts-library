# Add to Instacart cart

Automatically add to Instacart cart on instacart.com. Add an Instacart.com product to one store's cart, by store slug and product id, in the given quantity (added to any already in that cart). Returns that store's cart after the add, with a review_hash per line. Refuses a product the store does not sell, a store Instacart has not in this delivery area, or a total above the most Instacart allows per order. On a browser that does not keep Instacart's cookies between runs, the cart does not persist.

- Site: instacart.com
- Address: `reduck/instacart.com/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instacart.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instacart.com/add_to_cart
```

## Input

- `store` (string, required): The store's Instacart slug (e.g. "wegmans"), from Get Instacart product offers or the store's link.
- `product` (string, required): An Instacart product id or product link, from Search Instacart store products.
- `quantity` (integer, optional)

## Output

- `added` (object, required)
- `count` (number, required)
- `lines` (array, required)
- `store` (string, required)
- `cartId` (string, required)
- `total` (number | null, optional)

## FAQ

### What does "Add to Instacart cart" do?

Add an Instacart.com product to one store's cart, by store slug and product id, in the given quantity (added to any already in that cart). Returns that store's cart after the add, with a review_hash per line. Refuses a product the store does not sell, a store Instacart has not in this delivery area, or a total above the most Instacart allows per order. On a browser that does not keep Instacart's cookies between runs, the cart does not persist.

### How do I automatically add to Instacart cart on instacart.com?

Ask an AI agent connected to Reduck to run reduck/instacart.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instacart.com/add_to_cart

### Is there a instacart.com API to add to Instacart cart?

You do not need one. "Add to Instacart cart" drives the real instacart.com pages in a browser, so it works whether or not instacart.com offers an API for this.

### What information do I need to provide?

Required: store, product. Optional: quantity.

### What does it return?

It returns added, count, lines, store, total, cartId.

### Do I need to be logged in to instacart.com?

No. It only uses pages of instacart.com that are reachable without signing in.

### Does it change anything on instacart.com, or only read data?

It makes changes on instacart.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instacart.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instacart.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/instacart.com/add_to_cart
