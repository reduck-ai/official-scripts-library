# List Etsy cart items

Automatically list Etsy cart items on etsy.com. List the items in your Etsy (etsy.com) cart: for each line its listing id, inventory (variation) id, chosen option ids, title, shop, quantity, unit price, regular price, line total and availability, plus the cart's item count, items total, estimated shipping, total and currency. An empty cart returns an empty list. Saved-for-later items are not included.

- Site: etsy.com
- Address: `reduck/etsy.com/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/etsy.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/etsy.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Total quantity in the cart; 0 for an empty cart.
- `lines` (array, required)
- `total` (number | null, required): Cart total Etsy shows (items and estimated shipping) in the browser's currency; null for an empty cart.

## FAQ

### What does "List Etsy cart items" do?

List the items in your Etsy (etsy.com) cart: for each line its listing id, inventory (variation) id, chosen option ids, title, shop, quantity, unit price, regular price, line total and availability, plus the cart's item count, items total, estimated shipping, total and currency. An empty cart returns an empty list. Saved-for-later items are not included.

### How do I automatically list Etsy cart items on etsy.com?

Ask an AI agent connected to Reduck to run reduck/etsy.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/etsy.com/list_cart_items

### Is there a etsy.com API to list Etsy cart items?

You do not need one. "List Etsy cart items" drives the real etsy.com pages in a browser, so it works whether or not etsy.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to etsy.com?

No. It only uses pages of etsy.com that are reachable without signing in.

### Does it change anything on etsy.com, or only read data?

It only reads. It looks things up on etsy.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/etsy.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/etsy.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/etsy.com/list_cart_items
