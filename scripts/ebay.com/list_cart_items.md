# List eBay cart items

Automatically list eBay cart items on ebay.com. List the items in your eBay (ebay.com) cart: for each line its item id, variation, title, seller, condition, quantity, unit price, line total and shipping cost, plus the cart's item count, subtotal and currency, and whether it is this browser's guest cart. An empty cart returns an empty list. Saved-for-later items are not included.

- Site: ebay.com
- Address: `reduck/ebay.com/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ebay.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ebay.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Total quantity in the cart; 0 for an empty cart.
- `lines` (array, required)
- `total` (number | null, required): Cart subtotal eBay shows, items and shipping, in USD; null for an empty cart.

## FAQ

### What does "List eBay cart items" do?

List the items in your eBay (ebay.com) cart: for each line its item id, variation, title, seller, condition, quantity, unit price, line total and shipping cost, plus the cart's item count, subtotal and currency, and whether it is this browser's guest cart. An empty cart returns an empty list. Saved-for-later items are not included.

### How do I automatically list eBay cart items on ebay.com?

Ask an AI agent connected to Reduck to run reduck/ebay.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/list_cart_items

### Is there a ebay.com API to list eBay cart items?

You do not need one. "List eBay cart items" drives the real ebay.com pages in a browser, so it works whether or not ebay.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to ebay.com?

No. It only uses pages of ebay.com that are reachable without signing in.

### Does it change anything on ebay.com, or only read data?

It only reads. It looks things up on ebay.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ebay.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/ebay.com/list_cart_items
