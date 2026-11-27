# List Instacart cart items

Automatically list Instacart cart items on instacart.com. Read one store's cart on Instacart.com (each store has its own cart), by store slug: the cart id, item count, total of the item prices Instacart shows, and each line with its line id, product id, item id (offerId), name, store, quantity, unit price and line price in US dollars, plus a review_hash per line to pass to Remove from Instacart cart. An empty cart returns no lines.

- Site: instacart.com
- Address: `reduck/instacart.com/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instacart.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instacart.com/list_cart_items
```

## Input

- `store` (string, required): The store's Instacart slug, as in instacart.com/store/<slug> (e.g. "wegmans").

## Output

- `count` (number, required)
- `lines` (array, required)
- `store` (string, required)
- `total` (number | null, required)
- `cartId` (string, required)

## FAQ

### What does "List Instacart cart items" do?

Read one store's cart on Instacart.com (each store has its own cart), by store slug: the cart id, item count, total of the item prices Instacart shows, and each line with its line id, product id, item id (offerId), name, store, quantity, unit price and line price in US dollars, plus a review_hash per line to pass to Remove from Instacart cart. An empty cart returns no lines.

### How do I automatically list Instacart cart items on instacart.com?

Ask an AI agent connected to Reduck to run reduck/instacart.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instacart.com/list_cart_items

### Is there a instacart.com API to list Instacart cart items?

You do not need one. "List Instacart cart items" drives the real instacart.com pages in a browser, so it works whether or not instacart.com offers an API for this.

### What information do I need to provide?

Required: store.

### What does it return?

It returns count, lines, store, total, cartId.

### Do I need to be logged in to instacart.com?

No. It only uses pages of instacart.com that are reachable without signing in.

### Does it change anything on instacart.com, or only read data?

It only reads. It looks things up on instacart.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instacart.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instacart.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/instacart.com/list_cart_items
