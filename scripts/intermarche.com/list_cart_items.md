# List Intermarché cart items

Automatically list Intermarché cart items on intermarche.com. List the items in this browser's Intermarché.com cart for one store (guest or signed in): each line with its line id, barcode number, product id, name, seller, quantity, unit price and line price in euros, link, and its review_hash (pass it to Remove Intermarché product from cart), plus the item count and total. The store is its 5-digit code (for example 09571). An empty cart returns an empty list.

- Site: intermarche.com
- Address: `reduck/intermarche.com/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/intermarche.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/intermarche.com/list_cart_items
```

## Input

- `store` (string, required): Store code, 5 digits, e.g. 09571.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number, required)

## FAQ

### What does "List Intermarché cart items" do?

List the items in this browser's Intermarché.com cart for one store (guest or signed in): each line with its line id, barcode number, product id, name, seller, quantity, unit price and line price in euros, link, and its review_hash (pass it to Remove Intermarché product from cart), plus the item count and total. The store is its 5-digit code (for example 09571). An empty cart returns an empty list.

### How do I automatically list Intermarché cart items on intermarche.com?

Ask an AI agent connected to Reduck to run reduck/intermarche.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intermarche.com/list_cart_items

### Is there a intermarche.com API to list Intermarché cart items?

You do not need one. "List Intermarché cart items" drives the real intermarche.com pages in a browser, so it works whether or not intermarche.com offers an API for this.

### What information do I need to provide?

Required: store.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to intermarche.com?

No. It only uses pages of intermarche.com that are reachable without signing in.

### Does it change anything on intermarche.com, or only read data?

It only reads. It looks things up on intermarche.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/intermarche.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intermarche.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/intermarche.com/list_cart_items
