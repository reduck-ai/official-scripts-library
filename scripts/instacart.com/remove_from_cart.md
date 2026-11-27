# Remove from Instacart cart

Automatically remove from Instacart cart on instacart.com. Remove a product's whole line from one store's Instacart.com cart, by store slug and product id, after checking the line is still the one reviewed: pass the review_hash that List Instacart cart items gave for it. If the line changed (quantity or price), nothing is removed and the error gives the line as it is now and its new hash. Returns that store's cart after the removal.

- Site: instacart.com
- Address: `reduck/instacart.com/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instacart.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instacart.com/remove_from_cart
```

## Input

- `store` (string, required): The store's Instacart slug (e.g. "wegmans").
- `product` (string, required): The line's productId from List Instacart cart items.
- `review_hash` (string, required): The line's review_hash from List Instacart cart items.

## Output

- `count` (number, required)
- `lines` (array, required)
- `store` (string, required)
- `cartId` (string, required)
- `removed` (object, required)
- `total` (number | null, optional)

## FAQ

### What does "Remove from Instacart cart" do?

Remove a product's whole line from one store's Instacart.com cart, by store slug and product id, after checking the line is still the one reviewed: pass the review_hash that List Instacart cart items gave for it. If the line changed (quantity or price), nothing is removed and the error gives the line as it is now and its new hash. Returns that store's cart after the removal.

### How do I automatically remove from Instacart cart on instacart.com?

Ask an AI agent connected to Reduck to run reduck/instacart.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instacart.com/remove_from_cart

### Is there a instacart.com API to remove from Instacart cart?

You do not need one. "Remove from Instacart cart" drives the real instacart.com pages in a browser, so it works whether or not instacart.com offers an API for this.

### What information do I need to provide?

Required: store, product, review_hash.

### What does it return?

It returns count, lines, store, total, cartId, removed.

### Do I need to be logged in to instacart.com?

No. It only uses pages of instacart.com that are reachable without signing in.

### Does it change anything on instacart.com, or only read data?

It makes changes on instacart.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instacart.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instacart.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/instacart.com/remove_from_cart
